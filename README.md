# 📚 RAG-Based Document Chatbot

A local Retrieval-Augmented Generation (RAG) chatbot that allows users to upload PDF documents and ask natural-language questions about their content.

The chatbot processes the uploaded document, converts the content into vector embeddings, retrieves the most relevant information, and generates answers using a locally running LLM.

---

## 📌 Project Overview

This project implements a Retrieval-Augmented Generation (RAG) pipeline for document-based question answering.

Users can upload a PDF through a Streamlit interface and ask questions related to the uploaded document.

The system:

1. Extracts text from the PDF
2. Splits the document into smaller chunks
3. Generates vector embeddings
4. Stores the embeddings in ChromaDB
5. Performs semantic similarity search
6. Retrieves the most relevant document chunks
7. Sends the retrieved context to Gemma 2B
8. Generates an answer based only on the uploaded document

The project runs locally using Ollama and does not require a paid API.

---

## ✨ Features

- 📄 Upload PDF documents
- 🔍 Extract text from PDFs
- ✂️ Split documents into smaller chunks
- 🧠 Generate embeddings using Nomic Embed Text
- 🗄️ Store embeddings using ChromaDB
- 🔎 Perform semantic similarity search
- 🤖 Generate answers using Gemma 2B
- 💬 Interactive Streamlit chatbot interface
- 🔒 Local processing using Ollama
- 💰 No paid API required

---

## 🏗️ Architecture

```text
PDF Upload
     ↓
PDF Text Extraction
     ↓
Text Chunking
     ↓
Nomic Embed Text
     ↓
Vector Embeddings
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

Technologies Used
Technology	Purpose
Python	Core programming language
LangChain	RAG pipeline and document processing
PyPDF	PDF text extraction
Nomic Embed Text	Document embeddings
ChromaDB	Vector database
Ollama	Local model execution
Gemma 2B	Local language model
Streamlit	Web-based chatbot interface


📁 Project Structure
RAG-Document-Chatbot/
│
├── app.py
├── rag.py
├── test_rag.py
├── requirements.txt
├── README.md
├── .gitignore
└── venv/

⚙️ Installation
1. Clone the Repository
git clone https://github.com/Abhishekneeli/RAG-Document-Chatbot.git

Move into the project

cd RAG-Document-Chatbot

2. Create a Virtual Environment

On Windows:

python -m venv venv

Activate the environment:

.\venv\Scripts\Activate.ps1

If PowerShell gives an execution-policy error, run:

Set-ExecutionPolicy -Scope Process -ExecutionPolicy RemoteSigned

Then activate again:

.\venv\Scripts\Activate.ps1
3. Install Dependencies
pip install -r requirements.txt
🦙 Ollama Setup

This project uses Ollama to run the models locally.

Install Ollama on your computer.

Then download the embedding model:

ollama pull nomic-embed-text

Download the language model:

ollama pull gemma2:2b

Check the installed models:

ollama list

You should see:

nomic-embed-text
gemma2:2b
▶️ How to Run

Make sure the virtual environment is activated.

Run:

streamlit run app.py

Streamlit will start the chatbot application in your browser.

💬 How to Use
Step 1 — Upload a PDF

Open the Streamlit application and upload a PDF document.

Step 2 — Document Processing

The application will:

PDF
 ↓
Text Extraction
 ↓
Chunking
 ↓
Embeddings
 ↓
ChromaDB
Step 3 — Ask a Question

Enter a question related to the uploaded document.

For example:

What is the main topic of this document?
Step 4 — Generate Answer

The chatbot retrieves the most relevant document chunks and sends them to Gemma 2B.

Gemma then generates the final answer using the retrieved context.

🧪 Example Questions

You can ask questions such as:

What is the main topic of the document?

Explain the key concepts discussed in the document.

What are the important points mentioned in Chapter 2?

What are the advantages discussed in the document?

Summarize the section about machine learning.

What does the document say about artificial intelligence?
📸 Screenshots

Screenshots of the Streamlit application can be added here.

Example:

![RAG Chatbot](screenshots/chatbot.png)
🔄 RAG Workflow

The complete workflow is:

User uploads PDF
       ↓
PyPDF extracts document text
       ↓
RecursiveCharacterTextSplitter
       ↓
Document chunks
       ↓
Nomic Embed Text
       ↓
Vector embeddings
       ↓
ChromaDB
       ↓
User asks question
       ↓
Similarity Search
       ↓
Top relevant chunks
       ↓
Gemma 2B
       ↓
Final Answer
🔐 Local & Cost-Free Architecture

The project uses locally running models through Ollama.

Therefore:

No OpenAI API key is required
No paid LLM API is required
Documents can be processed locally
Embeddings are generated locally
LLM inference is performed locally
🚀 Future Improvements

Possible future improvements include:

Support for multiple PDF uploads
Support for DOCX and TXT files
Conversation memory
Source and page citations
Improved document retrieval
Hybrid search
Reranking retrieved documents
Streaming responses
Chat history
Docker deployment
Cloud deployment
Authentication and user management
🎯 Learning Outcomes

Through this project, I gained practical experience with:

Retrieval-Augmented Generation
Large Language Models
Vector databases
Semantic search
Document embeddings
LangChain
Ollama
ChromaDB
Streamlit
PDF document processing
End-to-end AI application development
👨‍💻 Author

Abhishek Neeli

AI & ML Graduate

📄 License

This project is intended for educational and portfolio purposes.


---

# Step 5 — Save the README

After pasting everything:

Press:

```text
Ctrl + S

That's it.