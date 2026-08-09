# RAG-Based Document Chatbot

A local Retrieval-Augmented Generation (RAG) chatbot that allows users to upload PDF documents and ask natural-language questions about their content.

## Features

- Upload PDF documents
- Extract text from PDFs
- Split documents into smaller chunks
- Generate embeddings using Nomic Embed Text
- Store embeddings in ChromaDB
- Retrieve relevant document chunks using semantic search
- Generate answers using Gemma 2B
- Local processing using Ollama
- No paid API required
- Batch processing for large PDF documents

## Technologies

- Python
- LangChain
- Ollama
- Gemma 2B
- Nomic Embed Text
- ChromaDB
- Streamlit
- PyPDF

## Architecture

PDF Upload  
↓  
PDF Text Extraction  
↓  
Text Chunking  
↓  
Nomic Embeddings  
↓  
ChromaDB  
↓  
Similarity Search  
↓  
Relevant Document Chunks  
↓  
Gemma 2B  
↓  
Generated Answer

## Project Structure

```text
RAG-Document-Chatbot/
│
├── app.py
├── rag.py
├── test_rag.py
├── requirements.txt
├── README.md
└── .gitignore