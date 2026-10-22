# Research-Paper-RAG-Assistant
AI assistant that answers questions about research papers using Retrieval-Augmented Generation (RAG), with source citations. PRISM project, in development.

# Research Paper RAG Assistant

An AI-powered assistant that lets you ask questions about research papers in plain language and get answers **grounded in the papers themselves**, with citations (paper, section and page) so every answer can be verified.

> **Status: Planning and design phase.** This project is part of the PRISM (Project Based Research for Innovative Solutions and Metamorphosis) course, Department of Computer Applications. The code is being added as development progresses.

## Problem

Reading and comparing research papers is slow. A single topic can have hundreds of papers, and finding a specific detail (a dataset, a method, a limitation) means reading each one. General chatbots can answer questions but are not tied to the papers you are reading. They can hallucinate facts or invent citations, which is a problem in academic work.

## Our Solution

A Retrieval-Augmented Generation (RAG) system that:

1. Takes research papers (PDF) as input
2. Extracts and splits the text into meaningful, section-aware chunks
3. Stores the chunks as vector embeddings
4. Retrieves the passages most relevant to your question
5. Generates an answer using only those passages, and shows the sources

## Planned Features

- Upload and process research papers (PDF)
- Question answering with citations (paper, section, page)
- Hybrid retrieval (keyword + semantic search)
- Paper summaries
- Side-by-side comparison of two or more papers
- Extraction of key details (problem, method, dataset, results, limitations)
- Simple web interface
- Evaluation of embedding models, chunk sizes and retrieval methods on scientific text

## Planned Architecture

```
PDF papers → Parsing & chunking → Embeddings → Vector store
                                                    ↓
User question → Retrieval (top-k passages) → LLM → Answer + citations
```

## Tech Stack (under evaluation)

| Part | Options being considered |
|---|---|
| Language | Python |
| PDF parsing | PyMuPDF, pdfplumber, GROBID |
| Framework | LangChain / LlamaIndex |
| Embeddings | sentence-transformers (BGE, E5, MiniLM) |
| Vector store | FAISS / ChromaDB |
| LLM | API-based or local (Ollama) |
| Interface | Streamlit / Gradio |

## Roadmap

- [x] Topic selection and problem definition
- [x] Initial literature and tools survey
- [ ] Prototype design and UI wireframes
- [ ] Document ingestion and chunking
- [ ] Embedding, vector storage and retrieval
- [ ] Answer generation with citations
- [ ] Web interface
- [ ] Testing and evaluation
- [ ] Documentation and final report

## Team

- Krishan Kanhya Kumawat
- Apireddy Babu Prakash Reddy

Department of Computer Applications, Kristu Jayanti (Deemed to be University)
Faculty Mentor: Dr. Rajalakshmi K

## License

To be decided.
