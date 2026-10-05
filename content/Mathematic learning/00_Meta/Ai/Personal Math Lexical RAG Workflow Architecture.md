---
title: Personal Math Lexical RAG Workflow Architecture
tags:
  - meta/architecture
  - rag/fts5-bm25
  - math/tools
  - system/workflow
created: 2026-08-05
updated: 2026-08-06
description: System architecture and operational workflow for FTS5 + BM25 Lexical RAG engine integrated with 4 doc_types, 2-layer LaTeX normalization, PDF page_num tracking, and tool signatures.
---

# 🏗️ Personal Math Lexical RAG Workflow Architecture (`FTS5 + BM25`)

Building a **Lexical RAG Workflow (FTS5 + BM25)** specifically tailored for a personal mathematical knowledge base (containing books, Obsidian notes, study sessions, and problem sets) requires leveraging SQLite FTS5's exact token matching alongside BM25's relevance ranking.

Because mathematical tools and techniques are often described using specific terms, LaTeX symbols, or explicit strategy names, FTS5 + BM25 provides precise, inspectable, and fast retrieval without the overhead, cost, or degradation of vector embeddings.

---

## 📐 System Architecture Overview

```mermaid
flowchart TD
    subgraph Phase1["1. Data Ingestion & Layout Parsing"]
        A["📁 Knowledge Vault (D:\personal knowledge)"] --> B{"Document Format"}
        B -- ".md Notes & Problems" --> C["Markdown Parser:\nFrontmatter, Hashtags & Header Split"]
        B -- ".pdf Books" --> D["Docling GPU VLM / PyPDF:\nLayout & Table Extraction"]
        C --> E["Math-Aware Atomic Chunker:\nPreserves Proofs & Adds Breadcrumbs\n[Book > Chapter > Section]"]
        D --> E
        E --> F["Document Classifier (4 Categories):\nnote | session | problem | book"]
    end

    subgraph Phase2["2. 2-Layer LaTeX Normalization & FTS5 Storage"]
        F --> G["LaTeX Normalizer:\nLayer 1: Symbol Dict (\\mathbb{R} -> MATH_SET_REAL)\nLayer 2: RegEx (\\vec{v}, \\mathbb{X}, \\frac{a}{b})"]
        G --> H[("SQLite FTS5 Table: math_fts\n(math_vault_fts.db)")]
        H --> I["Weighted Schema:\n- page_num UNINDEXED (w=0.0)\n- title (w=3.0)\n- tool_signature (w=2.5)\n- section_heading (w=1.5)\n- content (w=1.0)"]
    end

    subgraph Phase3["3. Lexical Retrieval & Query Expansion"]
        J["❓ User Query"] --> K{"Quoted Query?"}
        K -- '\"real number\"' --> L["Exact Phrase Search\n(No Synonym Expansion)"]
        K -- 'real number' --> M["Math Query Expander:\nSynonym Expansion + LaTeX Token Mapping"]
        L --> N["FTS5 BM25 Engine"]
        M --> N
        I <--> N
        N --> O["Top-K Ranked Passages with Page & Section Citations"]
    end

    subgraph Phase4["4. LLM RAG Prompt & Tactical Synthesis"]
        O --> P["RAG Prompt Builder"]
        P --> Q["LLM Synthesis Output:\n- Provenance (book/note/session/problem)\n- Page & Section Citations (Page X)\n- Trigger Pattern (When to apply)\n- Mathematical Mechanism & LaTeX Examples"]
    end
```

---

## 🛠️ Step 1: Database Schema & SQLite FTS5 Indexing Setup

To index mathematical content and prioritize mathematical tools, SQLite FTS5 is structured with **4 unindexed metadata fields**, **column weighting**, and **`unicode61` tokenization** supplemented by Python-side LaTeX pre-normalization.

### SQLite FTS5 Initialization (Python)
```python
import sqlite3

DB_NAME = "math_vault_fts.db"

def init_db(db_path=DB_NAME):
    """Initialize SQLite FTS5 virtual table for storing math notes, books, sessions, and problems."""
    conn = sqlite3.connect(db_path, timeout=30.0)
    cursor = conn.cursor()
    
    cursor.execute("""
        CREATE VIRTUAL TABLE IF NOT EXISTS math_fts USING fts5(
            file_path UNINDEXED,      -- Relative path to file (w=0.0)
            doc_type UNINDEXED,       -- 'note', 'session', 'problem', 'book' (w=0.0)
            page_num UNINDEXED,       -- PDF Page Number / Range 'Page 141-142' (w=0.0)
            title,                    -- Note title or document name (w=3.0)
            tool_signature,           -- Explicit math tools/tags (#tool/...) (w=2.5)
            section_heading,          -- Header section or breadcrumb (w=1.5)
            content,                  -- Normalized text / LaTeX / VLM output (w=1.0)
            tokenize = unicode61
        );
    """)
    conn.commit()
    return conn
```

---

## 🏷️ Step 2: 4-Category Document Classification (`doc_type`)

Documents across your vault are classified into **4 clean categories**:

| Document Type (`doc_type`) | Target Paths & Patterns | Role in Knowledge Base |
| :--- | :--- | :--- |
| **`note`** | `mathematic note/`, `01_Toolbox/`, formal subject notes | Formal mathematical notes, definitions, theorems, abstract tools. |
| **`session`** | `00_Sessions/`, `scratch/`, `workspace/` | Raw study workspace notes, problem attempts, question-theory linking. |
| **`problem`** | `04_Problems/`, `03_Examples/`, `exercise`, `tutorial`, `assignment` | Worked examples, problem sets, exercises, tutorials, exam questions. |
| **`book`** | `02_Books/`, `ebook/`, `.pdf` textbooks | Official reference textbooks, eBooks, reading materials. |

```python
def classify_doc_type(file_path):
    lower_path = file_path.lower()
    if any(k in lower_path for k in ["00_sessions", "session", "scratch", "workspace"]):
        return "session"
    if any(k in lower_path for k in ["04_problems", "03_examples", "example", "03_exam_questions", "exam", "paper", "assignment", "quiz", "test", "problem", "exercise", "tutorial"]):
        return "problem"
    if any(k in lower_path for k in ["02_books", "books", "textbook", "ebook"]):
        return "book"
    if any(k in lower_path for k in ["mathematic note", "01_notes", "01_toolbox", "notes", "mathematic learning", "obsidian vault"]):
        return "note"
    return "note" if file_path.endswith(".md") else ("book" if file_path.endswith(".pdf") else "general")
```

---

## 🧮 Step 3: 2-Layer LaTeX Pre-Normalization Engine

SQLite's default `unicode61` tokenizer strips punctuation and backslashes (`\`), converting `\mathbb{R}` into `mathbb` and `R`, or crashing FTS queries on raw `\`. 

To solve this, text is pre-processed before insertion into SQLite using a **2-Layer Normalizer**:

### Layer 1: Explicit Symbol Dictionary
Maps 40+ primary set, relation, operator, and logic symbols:
```python
LATEX_SYMBOL_MAP = {
    r"\mathbb{R}": " MATH_SET_REAL ",
    r"\mathbb{C}": " MATH_SET_COMPLEX ",
    r"\mathbb{Z}": " MATH_SET_INTEGER ",
    r"\subseteq": " MATH_REL_SUBSETEQ ",
    r"\int": " MATH_OP_INTEGRAL ",
    r"\perp": " MATH_REL_PERPENDICULAR ",
    r"\forall": " MATH_QUANT_FORALL ",
    r"\implies": " MATH_LOGIC_IMPLIES ",
}
```

### Layer 2: Dynamic RegEx Patterns
Catches arbitrary blackboard bold letters, vector decorators, and structural fractions automatically:
```python
def normalize_latex_text(text):
    if not text: return text
    normalized = text
    # Layer 1: Dictionary mapping
    for latex_sym, token in LATEX_SYMBOL_MAP.items():
        normalized = normalized.replace(latex_sym, token)
        
    # Layer 2: RegEx patterns
    normalized = re.sub(r"\\mathbb\{([A-Za-z])\}", r" MATH_SET_\1 ", normalized)
    normalized = re.sub(r"\\(?:vec|hat|bar|mathbf|tilde)\{([A-Za-z0-9]+)\}", r" \1 ", normalized)
    normalized = re.sub(r"\\frac\{([^}]+)\}\{([^}]+)\}", r" (\1 / \2) ", normalized)
    return normalized
```

---

## 📖 Step 4: PDF Page Number Tracking (`page_num`)

To cite exact PDF page numbers without breaking mathematical chunking:
1. Chunks remain **structural header chunks** (`## Section`, `> [!theorem]`) so math proofs are **never split** across page boundaries.
2. `page_num` is recorded as unindexed metadata (`Page 141–142` or `Page 142`).
3. Search outputs and LLM RAG prompts format the exact citation:
   `Source File: 02_Books/Linear_Algebra_Done_Right.pdf (BOOK - Page 142)`

---

## 🎯 Step 5: Tool Signatures & Note Writing Workflow

`tool_signature` is assigned a high **BM25 weight of 2.5**. You can tag notes in 3 ways:

1. **Frontmatter Header**:
   ```yaml
   ---
   tools: [add-zero-to-decouple, Gram-Schmidt]
   tags: [linear-algebra, inner-product]
   ---
   ```
2. **Inline Hashtags**: Type `#tool/add-zero-to-decouple` or `#linear-algebra` anywhere in daily notes.
3. **Callout Blocks**: Use `> [!tool] Tool Name` callouts.

---

## 🔍 Step 6: Query Expansion & BM25 Ranking Execution

```python
def search_math_vault(query, top_k=5, doc_type=None, db_path=DB_NAME):
    """Searches SQLite FTS5 table using Math Expansion, Page Tracking, and BM25 scoring."""
    conn = sqlite3.connect(db_path, timeout=30.0)
    cursor = conn.cursor()

    type_filter = "AND doc_type = ?" if doc_type else ""
    fts_query = expand_math_query(query)
    params = [fts_query, doc_type, top_k] if doc_type else [fts_query, top_k]

    sql = f"""
        SELECT file_path, doc_type, page_num, title, tool_signature, section_heading, content,
               bm25(math_fts, 0.0, 0.0, 0.0, 3.0, 2.5, 1.5, 1.0) AS score
        FROM math_fts
        WHERE math_fts MATCH ? {type_filter}
        ORDER BY score ASC
        LIMIT ?
    """
    cursor.execute(sql, params)
    return cursor.fetchall()
```

---

## 📊 Summary of System Upgrades

| Feature | Old Behavior | Upgraded RAG Architecture |
| :--- | :--- | :--- |
| **Doc Types** | 3 types (`note`, `book`, `exam`) | **4 clean categories** (`note`, `session`, `problem`, `book`) |
| **LaTeX Symbols** | `\mathbb{R}` stripped to `mathbb` + `R` (0 matches or syntax crash) | **2-Layer Normalizer** (`\mathbb{R}` $\rightarrow$ `MATH_SET_REAL`, RegEx dynamic patterns) |
| **PDF Page Tracking** | Missing or split page chunks | **Unbroken Structural Chunks** + `page_num UNINDEXED` metadata (`Page 142`) |
| **Search Types** | Broad search only | **Broad Concept Search** (`real number`) vs **Exact Literal Search** (`"real number"`) |
| **Tool Weighting** | Unweighted fields | **Weighted BM25** (`title`=3.0, `tool_signature`=2.5, `section_heading`=1.5, `content`=1.0) |

