# medical-rag-chatbot

---

# `Medical-rag-chatbot`

## Suggested Folder Structure
```text
medical-rag-chatbot/
├── README.md
├── requirements.txt
├── Dockerfile
├── .gitignore
├── app/
│   ├── main.py
│   ├── rag/
│   │   ├── ingest.py
│   │   ├── retriever.py
│   │   ├── embeddings.py
│   │   └── chain.py
│   ├── api/
│   │   └── routes.py
│   └── utils/
│       └── config.py
├── data/
│   └── sample_docs/
├── tests/
│   └── test_rag.py
├── docs/
│   └── architecture.png
└── ci/
    └── pipeline.md
```

# Medical RAG Chatbot

A Retrieval-Augmented Generation chatbot for document-grounded medical question answering using LangChain, FAISS, Docker, and API-based deployment.

## Overview
This project implements a RAG pipeline that ingests medical documents, creates embeddings, stores them in a FAISS vector index, and serves question-answering responses through an API.

## Features
- Document ingestion and chunking
- Embedding generation
- FAISS-based vector retrieval
- LangChain QA pipeline
- Dockerized deployment
- API endpoint for question answering

## Tech Stack
- Python
- LangChain
- FAISS
- FastAPI or Flask
- Docker
- AWS-ready deployment workflow

## Results
- Reduced document-grounded response retrieval time to under 2 seconds

## Project Structure
- `app/rag/` ingestion, embeddings, retriever, QA chain
- `app/api/` API endpoints
- `data/sample_docs/` example documents
- `tests/` retrieval and API tests

## Run Locally
```bash
git clone https://github.com/hossain-sanowar/medical-rag-chatbot
cd medical-rag-chatbot
pip install -r requirements.txt
python app/main.py
```
# Docker
```bash
docker build -t medical-rag-chatbot .
docker run -p 8000:8000 medical-rag-chatbot
```
Use Case

Designed as a production-style RAG reference system for medical document question answering.

Author

Md Sanowar Hossain
