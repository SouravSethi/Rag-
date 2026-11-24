# Research Papers RAG System

A Retrieval-Augmented Generation (RAG) system built to answer questions about machine learning research papers using LangChain, ChromaDB, and Groq LLM.

## 🎯 Project Overview

This project implements a question-answering system that can intelligently retrieve and answer questions from a collection of influential machine learning research papers. The system combines document retrieval with language generation to provide accurate, contextually relevant answers with source attribution.

## 📚 Research Papers Included

- **Attention Is All You Need** - The foundational Transformer architecture paper
- **BERT** - Bidirectional Encoder Representations from Transformers  
- **LLaMA** - Large Language Model Meta AI
- **LoRA** - Low-Rank Adaptation of Large Language Models
- **RAG Original** - Retrieval-Augmented Generation paper

## 🚀 Features

- **PDF Document Processing**: Automatic extraction and processing of research papers
- **Intelligent Chunking**: Smart text splitting with overlaps for better context preservation
- **Vector Search**: ChromaDB-powered semantic search with sentence transformers
- **Source Attribution**: Every answer includes source document and page references
- **Performance Scoring**: Built-in evaluation metrics for answer quality
- **Transparent Results**: Clear visualization of retrieval and generation process

## 🛠️ Technology Stack

- **LangChain**: Document processing and RAG pipeline orchestration
- **ChromaDB**: Vector database for semantic search
- **Sentence Transformers**: Text embeddings for document similarity
- **Groq**: High-performance LLM inference
- **PyPDF**: PDF text extraction
- **Python**: Core implementation language

## 📋 Prerequisites

- Python 3.8+
- Virtual environment (recommended)
- Groq API key

## ⚙️ Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd module6
   ```

2. **Create and activate virtual environment**
   ```bash
   python -m venv venv
   # Windows
   venv\Scripts\activate
   # Linux/Mac
   source venv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up environment variables**
   Create a `.env` file in the root directory:
   ```env
   GROQ_API_KEY=your_groq_api_key_here
   ```

## 🔧 Usage

### Running the Jupyter Notebook

1. **Start Jupyter**
   ```bash
   jupyter notebook
   ```

2. **Open [main.ipynb](main.ipynb)** and run the cells sequentially

### Key Components

The notebook demonstrates:
- **Document Loading**: PDF processing and text extraction
- **Text Chunking**: Intelligent splitting with metadata preservation  
- **Vector Store Creation**: Building ChromaDB index with embeddings
- **Question Answering**: RAG pipeline with source attribution
- **Performance Evaluation**: Answer quality scoring system

### Sample Questions

The system can answer questions like:
- "What is BERT and how does it work?"
- "Explain the self-attention mechanism in Transformers"
- "What are the key innovations of the Transformer architecture?"

## 📊 Project Structure

```
Rag/
├── main.ipynb              # Main implementation notebook
├── requirements.txt        # Python dependencies
├── analysis.md            # System strengths and weaknesses
├── reflection.md          # Challenges and improvements
├── rag_answers.txt        # Sample Q&A results with scores
├── research_papers/       # PDF documents
│   ├── Attention_Is_All_You_Need.pdf
│   ├── BERT_Paper.pdf
│   ├── Llama_Paper.pdf
│   ├── LoRA_Paper.pdf
│   └── RAG_Original.pdf
└── research_paper_db/     # ChromaDB vector store
    ├── chroma.sqlite3
    └── embeddings/
```

## 🎯 System Performance

### Strengths
- ✅ Provides relevant answers with proper source attribution
- ✅ Fast retrieval and response times
- ✅ Easy to extend for new document collections
- ✅ Transparent and verifiable results
- ✅ Scalable vector database architecture

### Current Limitations
- ⚠️ May retrieve partially relevant chunks for complex queries
- ⚠️ Limited reasoning across multiple documents
- ⚠️ Performance depends on chunking strategy quality
- ⚠️ Struggles with ambiguous or implicit questions

## 🔄 Potential Improvements

### Short Term
- Implement hybrid search (dense + BM25)
- Add answer confidence scoring
- Improve chunking strategies (semantic-based)
- Enhanced error handling and logging

### Long Term  
- Fine-tune domain-specific embedding models
- Integrate user feedback loops
- Add answer validation and reranking
- Multi-modal support for figures and tables

## 📈 Evaluation Metrics

The system includes built-in evaluation with scores for:
- **Context Quality** (1-5): Relevance of retrieved chunks
- **Answer Quality** (1-5): Accuracy and completeness  
- **Ground Truth** (1-5): Factual correctness
- **Overall Score**: Weighted average performance

## 🔗 References

- [LangChain Documentation](https://langchain.readthedocs.io/)
- [ChromaDB Documentation](https://docs.trychroma.com/)
- [Sentence Transformers](https://www.sbert.net/)
- [Groq API](https://groq.com/)
