# Transformer-Mini-RAG

**Transformer-Mini-RAG** is a minimal, educational implementation of Retrieval-Augmented Generation (RAG) using transformer models. The project demonstrates how to combine document retrieval with transformer-based text generation for question answering and information extraction tasks.

## Overview

Retrieval-Augmented Generation (RAG) pipelines improve the accuracy and faithfulness of language models by grounding their answers in external documents. This project walks through the key concepts and code for building a simple RAG system:

- **Chunking & Preprocessing:** Documents are split into token-sized chunks with overlap to preserve context. Metadata is added for improved retrieval.
- **Embeddings:** Text chunks are converted to dense vectors using transformer models (e.g., MiniLM, mpnet). Embeddings are stored and used for semantic search.
- **Vector Databases:** Embeddings are indexed using FAISS for fast nearest-neighbor retrieval.
- **Retrieval:** For a user query, relevant chunks are retrieved using cosine similarity over embeddings.
- **Generation:** Retrieved text chunks are augmented with the query and passed to a sequence-to-sequence transformer (e.g., T5) to generate an answer.
- **Evaluation & Guardrails:** Prompts, models, and indices are versioned. Metrics like faithfulness, relevancy, and latency are tracked. PII masking and safety filters are applied.

## Features

- Transformer-based embedding and generation (uses Hugging Face `transformers` library).
- PDF/text ingestion and preprocessing.
- Semantic search via FAISS vector database.
- Simple RAG pipeline for answering questions with document context.
- Example notebook showing all steps interactively.

## Usage

1. **Setup:** Clone the repository and open the Jupyter Notebook (`Transformer (1).ipynb`).
2. **Document Loading:** Paste raw text or upload a PDF to ingest document content.
3. **Chunking & Embedding:** Text is split into chunks and embedded using a transformer encoder.
4. **Indexing:** Embeddings are indexed with FAISS for efficient retrieval.
5. **Ask Questions:** Enter a query; relevant chunks are retrieved and fed to a transformer model to generate grounded answers.
6. **Inspect Outputs:** See answer, citations (chunk IDs), and performance metrics.

## Concepts Covered

- Self-attention, transformer basics
- Embeddings and semantic search
- Vector databases (FAISS)
- RAG pipeline: retrieval + generation
- Metadata and evaluation metrics
- Privacy, safety, and ethical handling

## Requirements

- Python 3
- Jupyter Notebook
- torch, transformers, faiss, pypdf

## License

This project is for educational purposes and does not include a license by default. Please add one if you intend to use or modify for production.

---

**Author:** [Srishti1805](https://github.com/Srishti1805)
