# DocuMind-AI-RAG-Powered-PDF-Question-Answering-System.
DocuMind AI is a Retrieval-Augmented Generation (RAG) application that allows users to upload PDFs and ask questions about their content. The system retrieves relevant document chunks from a vector database and uses a large language model to generate accurate, context-aware answers. .
# RAG PDF Question Answering System

## Overview
This project implements a **Retrieval-Augmented Generation (RAG)** system that allows users to ask questions about the contents of a PDF document. The system ingests a PDF, splits it into chunks, generates embeddings, stores them in a vector database, retrieves relevant chunks for a query, and uses an LLM to generate an answer based on the retrieved context.

The application consists of:
- **PDF ingestion pipeline**
- **Vector database storage**
- **Semantic search**
- **LLM-based answer generation**
- **Streamlit user interface**

---

## Features
- Upload and process PDF documents
- Automatic text chunking
- Embedding generation for semantic search
- Vector storage using Qdrant
- Retrieval of relevant document context
- Answer generation using Groq LLM
- Interactive Streamlit interface for querying PDFs
- Event-driven workflows using Inngest

---

## Tech Stack
- **Python**
- **FastAPI**
- **Streamlit**
- **Qdrant (Vector Database)**
- **Groq LLM**
- **Inngest**
- **Sentence Transformers (Embeddings)**
- **Docker (optional for Qdrant)**
  ## Folder Structure
  RAG Production App
│
├── main.py
├── streamlit_app.py
├── vector_db.py
├── data_loader.py
├── custom_types.py
├── requirements.txt
├── .env
└── README.md

---

## Installation

### 1. Clone the repository
```bash
git clone https://github.com/your-repo/rag-pdf-app.git
cd rag-pdf-app

---

## Installation

### 1. Clone the repository
```bash
git clone https://github.com/your-repo/rag-pdf-app.git
cd rag-pdf-app
2. Create virtual environment
python -m venv venv

Activate environment:

Windows

venv\Scripts\activate
3. Install dependencies
pip install -r requirements.txt
Environment Variables

Create a .env file in the project root.

GROQ_API_KEY=your_groq_api_key
Running Qdrant

Using Docker:

docker run -p 6333:6333 qdrant/qdrant
Running the Backend

Start the FastAPI server:

uvicorn main:app --reload
Running the Streamlit App
streamlit run streamlit_app.py
Workflow

Upload a PDF document.

The system extracts text and splits it into chunks.

Chunks are converted into embeddings.

Embeddings are stored in the vector database.

User submits a question.

The system retrieves the most relevant chunks.

The LLM generates an answer using the retrieved context.
Example Query
Question: What is the main topic of the document?

The system retrieves the most relevant text chunks and generates an answer using the LLM.

Requirements

Example requirements.txt:

fastapi
uvicorn
streamlit
qdrant-client
python-dotenv
sentence-transformers
groq
inngest
pydantic
Future Improvements

Support for multiple PDFs

Improved chunking strategies

Streaming responses

Authentication

Production deployment

UI improvements

Metadata filtering in vector search

License

This project is for educational and research purposes.


---

## Project Structure
