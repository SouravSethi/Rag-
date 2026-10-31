# Reflection: Project Challenges & Improvements

**Challenges:**
- Handling noisy or inconsistent PDF data, such as missing text, formatting issues, or unreadable pages, which affected extraction quality.
- Ensuring correct chunking and metadata extraction, especially when documents had variable structures or missing metadata fields.
- Managing API keys securely in production and avoiding accidental exposure in code or version control.
- Balancing chunk size and overlap to optimize retrieval accuracy without losing important context.
- Dealing with limited model reasoning, which sometimes led to shallow or incomplete answers.
- Debugging integration issues between different libraries and keeping dependencies up to date.

**Improvements:**
- Use more advanced retrievers (e.g., dense+BM25 hybrid search) to improve recall and answer relevance.
- Add answer validation, reranking, or confidence scoring to filter or prioritize better responses.
- Improve preprocessing and chunking strategies, possibly using semantic or sentence-based chunking instead of fixed-size.
- Integrate user feedback and active learning to iteratively refine the system.
- Enhance error handling and logging for easier debugging and monitoring.
- Explore fine-tuning embedding models or using domain-specific models for better performance.
