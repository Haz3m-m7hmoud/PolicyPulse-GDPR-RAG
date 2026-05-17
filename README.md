# ⚖️ PolicyPulse – GDPR Legal Q&A RAG System

PolicyPulse is a Retrieval-Augmented Generation (RAG) system designed to answer GDPR-related legal questions using official GDPR documents and guidelines.

The system retrieves the most relevant legal text chunks and generates precise, article-backed responses while reducing hallucinations through a fact-checking module.

---

## 🚀 Features

- 📄 Upload GDPR PDF documents
- ✂️ Token-based document chunking
- 🔍 Semantic retrieval using embeddings and vector search
- 🤖 LLM-powered legal question answering
- ✅ Fact-checking module for hallucination reduction
- 📊 Interactive Streamlit dashboard
- 📌 Retrieved chunk visualization with similarity scores

---

## 🏗️ System Architecture

### 1. Document Loader
Loads GDPR PDF documents using **PyPDFLoader**.

### 2. Text Chunking
Splits documents into overlapping chunks using **TokenTextSplitter**.

### 3. Embeddings & Vector Store
- Embedding Model: `all-MiniLM-L6-v2`
- Vector Database: **ChromaDB**

### 4. Retriever
Retrieves the most relevant chunks using semantic similarity search.

### 5. Generator
Uses **Llama-3.3-70B** via **Groq API** to generate grounded answers.

### 6. Fact Checker
Performs a second LLM verification pass to reduce hallucinations.

---

## 🛠️ Tech Stack

- Python
- Streamlit
- LangChain
- ChromaDB
- HuggingFace Embeddings
- Groq API
- Llama-3.3-70B
- Retrieval-Augmented Generation (RAG)

---

## 📂 Dataset

- Official GDPR Full Text (PDF)
- GDPR Guidelines Documents

---

## 💡 Example Questions

**Q:** Can I use customer email for marketing without consent?

**A:** The system retrieves relevant GDPR chunks and provides article-backed responses based only on the retrieved legal text.

---

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/policypulse-gdpr-rag.git
cd policypulse-gdpr-rag
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Create a `.env` file

```env
GROQ_API_KEY=your_api_key_here
```

### 4. Run the application

```bash
streamlit run app.py
```

---

## 📸 Project Demo

Add screenshots of the Streamlit interface here.

Example:
- Question answering interface
- Retrieved chunks
- Fact-check verification

---

## 📈 Future Improvements

- Add support for multiple legal documents
- Implement MMR retrieval
- Improve legal citation highlighting
- Deploy using Streamlit Cloud

---

## 👨‍💻 Author

**Hazem Mahmoud**