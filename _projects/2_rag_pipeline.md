---
layout: page
title: RAG Pipeline — Document Q&A System
description: Production-style Retrieval-Augmented Generation pipeline built without LangChain for full architectural transparency
img:
importance: 2
category: AI/ML Engineering
---

A retrieval-augmented generation pipeline built from scratch without LangChain, prioritizing full debuggability and architectural transparency over convenience abstractions.

Technical stack: Python, PyMuPDF, sentence-transformers (all-MiniLM-L6-v2), ChromaDB, Azure OpenAI GPT-4o-mini

Architecture:

- **Parsing:** PyMuPDF for PDF ingestion and text extraction
- **Embedding:** sentence-transformers for dense vector representations
- **Storage:** ChromaDB as the vector database
- **Generation:** Azure OpenAI GPT-4o-mini for answer synthesis

Each component — parser, embedder, retriever, generator — is hand-rolled and independently testable. Custom chunking and top-k retrieval logic allow full control over pipeline behavior without black-box dependencies.
