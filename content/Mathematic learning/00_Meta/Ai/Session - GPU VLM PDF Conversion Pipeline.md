---
title: "Session: GPU VLM PDF Conversion Pipeline"
tags:
  - meta/session
  - system/workflow
  - rag/docling
  - gpu/rtx4050
created: 2026-08-05
description: Session notes for setting up and optimizing the Docling GPU VLM pipeline for converting math textbook PDFs into clean LaTeX Markdown.
---

# 🖥️ Session: GPU VLM PDF Conversion Pipeline

**Date**: 2026-08-05  
**Branch**: `math-deconstructor-local-version` → merged to `main`  
**Commit**: `b55daac`

---

## 🎯 Goal

Convert math textbook PDFs (e.g. *Linear Algebra Done Right*, 4th Ed.) into clean Markdown with **decoded LaTeX formulas** using Docling's VLM model (`CodeFormulaV2`) on the **NVIDIA GeForce RTX 4050 Laptop GPU**.

---

## 🔧 Script

**File**: `.agents/skills/personal-math-rag/scripts/convert_pdf_to_md.py`

```powershell
# Convert a single chapter by page range
python .agents/skills/personal-math-rag/scripts/convert_pdf_to_md.py `
  --pdf "D:\personal knowledge\ebook\<book>.pdf" `
  --out "D:\personal knowledge\Math Vault\Personal Knowledge\02_Books" `
  --pages "19-44"

# Batch convert entire ebook folder
python .agents/skills/personal-math-rag/scripts/convert_pdf_to_md.py
```

---

## 🐛 Problems Encountered & Fixes

### 1. CPU-Only PyTorch (No CUDA)
- **Symptom**: VLM running on CPU, extremely slow, out of memory.
- **Diagnosis**: `torch.cuda.is_available()` returned `False`.
- **Fix**: Reinstalled PyTorch with CUDA 12.1:
  ```powershell
  pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121
  ```

### 2. `os error 1455` — Windows Pagefile Too Small
- **Symptom**: Crash when loading `CodeFormulaV2` checkpoint (~2.5 GB).
- **Diagnosis**: Windows pagefile had only 2.4 GB free. `safe_open()` in HuggingFace requires contiguous virtual memory ≥ model size.
- **Fix**: Expanded Windows Virtual Memory on C: drive:
  - Initial: **8192 MB**, Maximum: **16384 MB**

### 3. Slow Weight Loading — 8-bit Quantization Default
- **Symptom**: Weight loading at ~392 it/s (vs ~1800+ it/s possible).
- **Diagnosis**: Default `AutoInlineVlmEngineOptions` used `load_in_8bit=True` (bitsandbytes). This is slower than fp16 on RTX GPUs.
- **Fix**: Switched to explicit `TransformersVlmEngineOptions`:
  ```python
  TransformersVlmEngineOptions(
      device="cuda",
      load_in_8bit=False,
      torch_dtype="float16",
      compile_model=True,
      use_kv_cache=True,
  )
  ```
- **Result**: **4–5× faster** weight loading.

### 4. Pydantic Validation Errors (2 bugs)
| Field | Wrong Value | Correct Value |
|:---|:---|:---|
| `device` | `"cuda:0"` | `"cuda"` |
| `torch_dtype` | `torch.float16` (object) | `"float16"` (string) |

### 5. Page Range — 0-indexed vs 1-indexed
- **Symptom**: `ValueError: Invalid page range: start must be ≥ 1`.
- **Fix**: Docling's `page_range` is **1-indexed**. Changed script to pass `(int(start), int(end))` directly.

### 6. Aligned Equations Not Rendering
- **Symptom**: Multi-line `$$...$$` blocks with `&` alignment rendered as broken equations.
- **Fix**: Added post-processing to auto-wrap aligned equation blocks:
  ```python
  if '&' in inner and '\\\\' in inner:
      inner = f'\\begin{{aligned}}\n{inner.strip()}\n\\end{{aligned}}'
  ```

---

## 📊 Performance Profile

| Phase | Duration | Note |
|:---|:---|:---|
| GPU cold start (weight loading) | ~5–10 sec | One-time per script run |
| Per page (formula-dense math) | ~7–8 sec/page | RTX 4050 + float16 |
| 26-page chapter (Ch. 1) | ~3.5 min | Vector Spaces |
| Full 408-page textbook (est.) | ~50–55 min | Run overnight |

---

## 📚 Linear Algebra Done Right — PDF Chapter Map

| Chapter | PDF Pages |
|:---|:---|
| Ch 1 — Vector Spaces | 19–44 |
| Ch 2 — Finite-Dimensional Vector Spaces | 45–68 |
| Ch 3 — Linear Maps | 69–136 |
| Ch 4 — Polynomials | 137–149 |
| Ch 5 — Eigenvalues & Eigenvectors | 150–198 |
| Ch 6 — Inner Product Spaces | 199–244 |
| Ch 7 — Operators on Inner Product Spaces | 245–314 |
| Ch 8 — Operators on Complex Vector Spaces | 315–349 |
| Ch 9 — Multilinear Algebra & Determinants | 350–400 |

> Page map extracted via `pdf-scanner` skill using PDF bookmark outline.

---

## ⚠️ Known Limitations

1. **`𝐅 𝑛 𝑛` superscript duplication** — PyPdfium misreads bold Unicode superscripts (e.g. `𝐅ⁿ` → `𝐅 𝑛 𝑛`). Text layer limitation, unfixable without a different backend.
2. **VLM hallucination on proof blocks** — Docling's formula detector sometimes misidentifies proof headers and sidebars as formula regions. The VLM then produces nonsense LaTeX (e.g. `\underbrace`, `\sqcup`). Occurs in ~5–10% of blocks.
3. **Multi-column TOC** — Table of contents pages render as markdown table/code block due to 2-column PDF layout. Not a concern for RAG usage.

---

## ✅ Output Quality

- **Clean formulas** (95%+): Standard equations, definitions, theorems decode correctly.
- **Aligned multi-line equations**: Fixed with `\begin{aligned}...\end{aligned}` post-processing.
- **RAG-ready**: BM25 keyword search works correctly despite minor formatting artifacts.

---

## 🔗 Related Files

- [[Personal Math Lexical RAG Workflow Architecture]]
- Script: `.agents/skills/personal-math-rag/scripts/convert_pdf_to_md.py`
- Output: `Personal Knowledge/02_Books/`
