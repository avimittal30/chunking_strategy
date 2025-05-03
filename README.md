# 🧠 Annual Report Chunking Strategies for RAG-Based Applications

This repository explores various text chunking strategies to optimize retrieval from annual reports, particularly for use in Retrieval-Augmented Generation (RAG) applications.

## 📌 Objective

To determine the most effective chunking approach for processing annual reports, aiming to retrieve the most relevant information for downstream tasks like summarization, question-answering, or report analysis.

## 🧪 Chunking Strategies Explored

### 1. Fixed-Length Chunking
- **Description:** Splits text into chunks based on a fixed number of tokens or characters.
- **Performance:** 
  - Retrieved relevant chunks.
  - However, **ranking was suboptimal** — the most relevant chunks often appeared lower in the retrieval results.

### 2. Sentence-Based Chunking
- **Description:** Splits text by complete sentences while maintaining semantic boundaries.
- **Performance:** 
  - Delivered the **best performance** overall.
  - Consistently **retrieved and ranked the most relevant chunks at the top**.
  - Preserved context without unnecessary overlap or loss of meaning.

### 3. Semantic Chunking
- **Description:** Used embeddings to group semantically similar sentences or paragraphs.
- **Performance:**
  - **Failed** in this use case.
  - Retrieved chunks were generally **not relevant**.
  - Over-aggregation of context resulted in diluted relevance.

## ✅ Conclusion

**Sentence-based chunking** emerged as the **most effective strategy** for this task. It provided precise and highly relevant retrieval results, outperforming both fixed-length and semantic chunking methods.

---

Feel free to explore the code and experiment further with different documents and chunking strategies!
