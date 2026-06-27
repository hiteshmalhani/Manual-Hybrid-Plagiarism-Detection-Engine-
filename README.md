# Manual-Hybrid-Plagiarism-Detection-Engine-
A transparent, locally deployable plagiarism detection system that detects verbatim copying and paraphrasing using a hybrid pipeline of Sentence-Transformer semantic similarity and Jaccard lexical shingling — all implemented from scratch in Python, powered by a FastAPI backend and React frontend.
Here's a clean GitHub project description you can use:

---

**Manual Hybrid Plagiarism Detection Engine**

A transparent, fully local plagiarism detection system that combines **semantic similarity** and **lexical matching** to catch both verbatim copying and paraphrasing.

Built without black-box libraries — every core algorithm (cosine similarity, 3-word shingling, Jaccard similarity) is implemented from scratch using pure Python and NumPy.

**How it works:**
- **Phase 1:** Converts text into 384-dim vectors via Sentence-Transformers and retrieves the top 5 semantically similar documents from a 20,000-document corpus using manual cosine similarity.
- **Phase 2:** Runs Jaccard similarity on 3-word shingle sets across 5 CPU cores in parallel using `ProcessPoolExecutor`.

**Tech Stack:** FastAPI · React/Vite · NumPy (memory-mapped) · Sentence-Transformers · Python multiprocessing

**Key highlights:**
- No external APIs — runs 100% locally, full data privacy
- Color-coded dashboard: 🔴 exact matches · 🟡 paraphrased content
- Corpus of ~20,000 documents (20 Newsgroups dataset)
- Flat RAM usage via memory-mapped `.npy` embeddings

> Built as a Text Mining course project to demonstrate NLP concepts through transparent, auditable implementation.

---

You can paste this directly into your GitHub repo's `README.md` or the repository description field.
