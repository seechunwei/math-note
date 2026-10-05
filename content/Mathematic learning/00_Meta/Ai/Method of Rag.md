Your sources present two highly innovative, lightweight alternatives to traditional "dense vector" Retrieval-Augmented Generation (RAG). Both approaches share a common goal: **bypassing the complexity, high maintenance, and black-box nature of traditional vector databases** in favor of simpler, more inspectable, and cost-effective architectures.

However, they achieve this goal using entirely different paradigms:

1. **Lexical-Retrieval RAG (using SQLite FTS5 & BM25)**
2. **File-System & Markdown-Based "RAG" (using Obsidian & Claude Code)**

---

### Method 1: Lexical-Retrieval RAG (FTS5 + BM25)

This method is a structured, database-driven approach that relies on classic information retrieval techniques rather than neural network embeddings.

- **How it Works:** The system indexes documents (such as PDFs and Obsidian notes) using **SQLite's FTS5 full-text search extension**. When a query is made, it applies the **BM25 scoring algorithm** to calculate a relevance score for each text segment based on term frequency and document length, retrieving the top-ranked segments for the LLM to use as context.
- **Key Strengths:**
    - **High Literal Stability:** It is incredibly reliable when searching for specific, exact literal clues such as **book titles, authors, theorem names, formulas, exact sentences, chapters, or page numbers**.
    - **Inspectability:** The matching logic is fully transparent. Developers can easily verify _why_ a document was retrieved based on exact keyword matches rather than trying to decipher high-dimensional vector math.
    - **Resilience to Formatting & OCR Errors:** Mathematical symbols, rare proper nouns, and OCR misreadings can severely degrade vector embedding representations, but lexical search handles them far more robustly.
    - **Zero-Overhead Maintenance:** Traditional dense retrieval requires you to select embedding models, configure chunking rules, and maintain a vector index. If you change your embedding model, you must re-encode your entire dataset—a limitation that FTS5/BM25 completely avoids.

---

### Method 2: File-System & Markdown-Based "RAG" (Obsidian)

Inspired by Andrei Karpathy, this method is a highly human-centric, flat-file approach that leverages an LLM's native capability to structure and navigate directories.

- **How it Works:** Rather than using a database, this method organizes data inside an **Obsidian Markdown vault** using a highly structured, hierarchical file system:
    1. **Staging (`/raw`):** Raw articles, PDFs, and papers are clipped or dumped here.
    2. **Wiki Generation (`/wiki`):** On demand, an AI agent (like Claude Code) reads the raw staging folder, synthesizes the information, and creates structured topic wikis, linking files together using native Obsidian Wiki-links.
    3. **Indexing (`master index`):** The LLM automatically maintains a central master index markdown file of all wikis, and each wiki subdirectory contains its own local index file.
    4. **Traversal:** When asked a question, the LLM reads the central index, routes to the correct sub-wiki index, identifies the exact file path, and reads only the necessary markdown files.
- **Key Strengths:**
    - **No Technical Overhead:** It requires **no vector database, no embedding models, and no complex retrieval code**. It is extremely lightweight, essentially free, and fast to deploy.
    - **Human-in-the-Loop Frontend:** Because Obsidian acts as the UI, the entire knowledge base is fully visible and readable to human eyes in real-time. It is never locked away in a "black box" database.
    - **Token Efficiency:** By training the LLM (via rules in a `Claude.md` file) to traverse indices systematically, the AI avoids wasting tokens loading massive, unrelated files or executing heavy search tool calls.

---

### Side-by-Side Comparison

|Feature|Lexical RAG (FTS5 + BM25)|Obsidian "RAG" (Karpathy Method)|
|:--|:--|:--|
|**Core Technology**|SQLite FTS5 index & BM25 statistical scoring.|Local Markdown file structure, native wiki-links, and LLM index-traversal.|
|**Retrieval Mechanism**|Computes algorithmic keyword matching scores across indexed text chunks.|Sequentially navigates human-readable index files (`master index` → `topic index` → `markdown file`).|
|**Data Ingestion**|Automated indexing of raw texts and PDFs.|Raw files are staged, then curated/summarized by the LLM into structured "wikis".|
|**Transparency**|High. Match reasons are easily auditable via SQL queries and keyword scoring.|Extremely High. The user can view, edit, and navigate the entire document network visually via Obsidian.|
|**Ideal Use Case**|Searching dense, unstructured books, math-heavy PDFs, and raw text corpus for exact formulas/literals.|Individual or small-team knowledge management, research synthesis, and cross-topic brainstorming.|
|**Scale Limits**|Highly scalable to medium and large document sizes.|Excellent for small-to-medium vaults, but struggles to scale to millions of documents due to LLM traversal limits.|

---

### Strategic Synthesis: When to Use Which?

- **Choose Lexical RAG (FTS5 + BM25)** if you have a massive library of raw documents (like hundreds of PDFs, textbooks, or scanned manuals) that contain highly precise technical terminology, codes, or formulas. This approach is ideal when you need to quickly pinpoint exact pages or paragraphs without spending human or AI effort to manually summarize or curate them first.
- **Choose Obsidian "RAG"** if you are a solo developer or a small team curating a highly interconnected body of research. It is perfect if you want to actively read, edit, and organize the knowledge yourself alongside the AI, relying on the LLM to write summaries and maintain the indexes as the vault grows.

_Interestingly, the two systems are not mutually exclusive._ As shown in your sources, you can actually use the **FTS5/BM25 pipeline to index your Obsidian notes**, giving you the visual curation of a wiki layout combined with the precise keyword retrieval power of a database.

---

🛠️ I can write a Python script to set up a mock SQLite database in your workspace, configure an FTS5 table, and demonstrate how BM25 scores are calculated against sample texts so you can see how it works firsthand.