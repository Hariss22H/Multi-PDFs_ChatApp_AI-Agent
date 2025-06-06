# 🤖 Multi-PDFs Chat Agent using Gemini AI

A Streamlit-powered AI chatbot that lets users upload and interact with **multiple PDF files** using **Google's Gemini AI**. It enables context-aware Q&A over documents using semantic search and conversational reasoning.

---

## 📌 Project Overview

This project creates an **AI-powered PDF assistant** that extracts knowledge from multiple uploaded PDFs and answers user queries using **Gemini embeddings** and **LLMs** via LangChain.  
It leverages **FAISS** for semantic search and provides an intuitive **Streamlit interface** for seamless interaction.

---

## 🚀 Features

- 📄 **Multi-PDF Upload & Parsing**
- 🤖 **Conversational Q&A Agent** (context-aware)
- 🧠 **Gemini Embeddings** for semantic chunking
- 🔍 **FAISS Vector DB** for fast similarity search
- 🗂️ **LangChain QA Chain** for accurate responses
- 🌐 **Streamlit Web UI** – clean and easy to use
- 📊 **Gemini Model Viewer** (via `check_models.py`)

---

## 📂 Dataset

No external dataset required. Users upload their own **PDF files** dynamically via the UI.  
Internally, the system extracts text, chunks it, embeds the chunks, stores them in FAISS, and performs real-time semantic retrieval.

---

## 🏗️ Architecture Overview

- **PDF Extraction:** `PyPDF2` reads all uploaded pages.
- **Chunking:** `RecursiveCharacterTextSplitter` from LangChain.
- **Embeddings:** Google’s `embedding-001` model (Gemini).
- **Vector Storage:** FAISS local DB.
- **LLM Model:** Gemini `gemini-1.5-pro-latest`.
- **Prompt:** Custom chain for accurate and safe answers.
- **Frontend:** Streamlit app with sidebar UI.

---

## 📊 Performance

- ✅ Near-instant response after processing
- ✅ Accurate answers based on embedded context
- ❌ Will not hallucinate outside provided PDFs
- 📉 Performance depends on PDF quality and content density

---

## 📁 Project Structure

```text
Multi-PDFs_ChatApp_AI-Agent-main/
├── chatapp.py                  # Main Streamlit App
├── check_models.py             # Gemini model lister
├── requirements.txt            # Python dependencies
├── .env                        # API key config (DO NOT COMMIT)
├── img/
│   ├── Robot.jpg
│   └── ChatGPT Image Apr 14, 2025.png
├── faiss_index/                # Auto-generated FAISS vector index
└── README.md

```
## 🛠 Installation & Setup
### 1️⃣ Clone the Repository
```bash
git clone https://github.com/YOUR_USERNAME/MultiPDF-ChatAgent.git
cd MultiPDF-ChatAgent
```
### 2️⃣ Install Dependencies
```bash
pip install -r requirements.txt
```
### 3️⃣ Google API Key
```bash
GOOGLE_API_KEY=your_actual_key
```
### 4️⃣ Deploy with Streamlit
```bash
 streamlit run chatapp.py
```

## ⚠️ Important
- Do NOT commit your .env file.
- To keep it out of version control, add this line to .gitignore:
```bash
   echo ".env" >> .gitignore
```
## 🛠 Future Enhancements
-🗂 Support for DOCX, TXT files

-🧾 Summarization of PDF content

-🗣 Voice-based querying

-🔐 User authentication & session storage

-📜 Auto-report generation from conversations

## 👨‍💻 Contributors
- **SHAIK HARRISS RAZVI** -Developer, Prompt Designer, UI/UX, Deployment

## 💡 Acknowledgments
-Google Generative AI (Gemini)

-LangChain

-Streamlit

-FAISS by Facebook AI Research

**⭐ star this repo** if you found it useful — and level up your PDFs with AI! 🔥

