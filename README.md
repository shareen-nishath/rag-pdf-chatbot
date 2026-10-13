# 📄 PDF Intelligence — RAG Chatbot

An AI-powered PDF Question Answering application built using Retrieval-Augmented Generation (RAG). Users can upload PDF documents, process their contents, and ask questions through an interactive web interface.

The application retrieves relevant information from the uploaded document and uses a Large Language Model (LLM) to generate contextual answers.

## ✨ Features

* 📄 Upload PDF documents directly through the web interface.
* 🧠 Extract text from PDF files.
* ✂️ Split document text into manageable chunks.
* 🔎 Retrieve relevant document sections using semantic search.
* 📚 Store document embeddings in ChromaDB.
* 🤖 Generate answers using Groq AI.
* 💬 Interactive chatbot interface built with Gradio.
* 🔄 Upload and process different PDFs.
* 🎨 Modern interface with a professional design.

## 🛠️ Technologies Used

* **Python** — Core programming language.
* **LangChain** — RAG pipeline and component integration.
* **Groq API** — Large Language Model inference.
* **OpenAI GPT-OSS 20B via Groq** — Language model used to generate answers.
* **Hugging Face Sentence Transformers** — Text embeddings.
* **ChromaDB** — Vector database for similarity search.
* **PyPDF** — PDF text extraction.
* **Gradio** — Interactive web interface.

## ⚙️ How It Works

1. **PDF Upload:** The user uploads a PDF through the web interface.
2. **Text Extraction:** PyPDF extracts text from the document.
3. **Text Splitting:** LangChain divides the extracted text into smaller chunks.
4. **Embedding Generation:** A Sentence Transformers model converts text chunks into numerical embeddings.
5. **Vector Storage:** ChromaDB stores the embeddings for efficient similarity search.
6. **Retrieval:** The retriever identifies relevant chunks based on the user's question.
7. **Answer Generation:** Groq AI generates an answer using the retrieved context.
8. **Display:** The answer appears in the Gradio chatbot interface.

## 📁 Project Structure

```text
pdf-intelligence-rag/
│
├── app.py
├── requirements.txt
└── README.md
```

## 🚀 Installation and Setup

### 1. Clone the Repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

Navigate into the project folder:

```bash
cd pdf-intelligence-rag
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Configure the Groq API Key

Obtain an API key from the Groq Console:

https://console.groq.com/

Set the API key as an environment variable.

**Windows PowerShell:**

```powershell
$env:GROQ_API_KEY="your_groq_api_key"
```

**Linux or macOS:**

```bash
export GROQ_API_KEY="your_groq_api_key"
```

Replace `your_groq_api_key` with your actual API key.

Never upload your API key to GitHub.

### 4. Run the Application

```bash
python app.py
```

Open the local Gradio URL displayed in the terminal.

## 💡 How to Use

1. Open the PDF Intelligence web application.
2. Upload a PDF document.
3. Click **Process PDF**.
4. Wait for the document processing confirmation.
5. Enter a question about the uploaded PDF.
6. Click **Ask AI**.
7. Read the generated answer.
8. Upload another PDF when you want to work with a different document.

## 🧠 Embedding Model

The application uses:

`sentence-transformers/all-MiniLM-L6-v2`

This model generates text embeddings that help identify semantically relevant document sections.

## 🤖 Language Model

The application uses:

`openai/gpt-oss-20b`

The model is accessed through the Groq API to generate answers from retrieved document context.

## 🔍 Retrieval-Augmented Generation (RAG)

RAG combines document retrieval with language generation.

Instead of relying only on the language model's existing knowledge, the application retrieves relevant information from the uploaded PDF and supplies it as context for answering questions.

This helps the chatbot provide document-specific answers and reduces unsupported responses.

## ⚠️ Limitations

* Text-based PDFs are supported; scanned PDFs may require OCR.
* Answers depend on the quality and content of the uploaded document.
* Very large PDFs may require additional processing time and memory.
* The application processes one active PDF at a time.
* The model may occasionally produce inaccurate answers, so important information should be verified against the original document.
* A valid Groq API key and internet connection are required.

## 🔒 Security

* Keep API keys private.
* Do not commit credentials to version control.
* Avoid uploading confidential or sensitive documents to publicly accessible deployments.
* Review the hosting platform's privacy and file-retention policies before deploying.

## 👩‍💻 Author

**Shareen Nishath**

B.Tech Artificial Intelligence and Data Science

## 📜 License

This project is intended for educational and demonstration purposes. Add a suitable open-source license if you plan to distribute the project publicly.
