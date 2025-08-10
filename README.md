# 📚 ChatWithPDF

A powerful AI-powered PDF chat application that allows you to upload PDFs and ask questions about their content. Built with FastAPI backend and Streamlit frontend.

## ✨ Features

- **PDF Processing**: Extract text, tables, and images from PDFs
- **AI Chat**: Ask questions about your PDF content using Groq LLM
- **Smart Retrieval**: Uses LangChain with ChromaDB for intelligent document search
- **Beautiful UI**: Modern Streamlit interface with excellent readability
- **Real-time Processing**: Instant answers with source citations

## 🏗️ Architecture

- **Backend**: FastAPI server (`main.py`) - Handles PDF processing and AI queries
- **Frontend**: Streamlit app (`app.py`) - User interface for file upload and chat
- **AI Engine**: LangChain + Groq + ChromaDB for intelligent document understanding

## 🚀 Quick Start

### Prerequisites
- Python 3.8+
- Virtual environment (recommended)

### Installation

1. **Clone and setup**:
```bash
git clone <your-repo-url>
cd ChatWithPDF
```

2. **Create virtual environment**:
```bash
python -m venv venv
venv\Scripts\activate  # Windows
# source venv/bin/activate  # Linux/Mac
```

3. **Install dependencies**:
```bash
pip install -r requirements.txt
```

4. **Set up environment variables** (optional):
Create a `.env` file in the root directory:
```env
GROQ_API_KEY=your_groq_api_key_here
GOOGLE_API_KEY=your_google_api_key_here
```

### Running the Application

**You need TWO terminal windows:**

#### Terminal 1 - Backend (FastAPI)
```bash
venv\Scripts\activate
python main.py
```
✅ Backend will start at: http://localhost:8000

#### Terminal 2 - Frontend (Streamlit)
```bash
venv\Scripts\activate
streamlit run app.py
```
✅ Frontend will open at: http://localhost:8501

## 📖 How to Use

1. **Upload PDF**: Use the sidebar to upload your PDF file
2. **Process PDF**: Click "🚀 Process PDF" to extract content
3. **Ask Questions**: Type questions in the chat interface
4. **Get Answers**: Receive AI-powered answers with source citations

## 🎯 Sample Questions

- "What is the main topic of this document?"
- "Can you summarize the key findings?"
- "What are the main conclusions?"
- "Explain the methodology used"
- "What are the limitations mentioned?"

## 🛠️ Project Structure

```
ChatWithPDF/
├── main.py              # FastAPI backend server
├── app.py               # Streamlit frontend
├── requirements.txt     # Python dependencies
├── README.md           # This file
└── venv/               # Virtual environment
```

## 🔧 Dependencies

- **FastAPI**: Modern web framework for APIs
- **Streamlit**: Web app framework for data science
- **LangChain**: LLM application framework
- **ChromaDB**: Vector database for embeddings
- **unstructured**: PDF processing and extraction
- **Groq**: Fast LLM inference

## 🚨 Troubleshooting

### Common Issues

1. **"streamlit command not found"**
   - Make sure to activate virtual environment first: `venv\Scripts\activate`

2. **"API server not running"**
   - Ensure `python main.py` is running in Terminal 1
   - Check if port 8000 is available

3. **PDF processing fails**
   - Check if PDF file is valid and not corrupted
   - Ensure all dependencies are installed correctly

4. **No answers from AI**
   - Verify your API keys in `.env` file
   - Check backend logs for errors

### Port Conflicts

If ports are already in use:
- Backend: Change port in `main.py` (line 389)
- Frontend: Change port in `streamlit run app.py --server.port 8502`

## 📝 API Endpoints

- `GET /` - Root endpoint
- `POST /upload-pdf` - Upload and process PDF
- `POST /ask` - Ask questions about processed PDF
- `GET /files` - List processed files
- `GET /health` - Health check

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## 📄 License

This project is licensed under the MIT License.

## 🙏 Acknowledgments

- Built with Streamlit and FastAPI
- Powered by LangChain and Groq
- PDF processing with unstructured library
