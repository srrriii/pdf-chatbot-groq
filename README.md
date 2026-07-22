# pdf-chatbot-groq
AI-powered PDF Question Answering chatbot built with Python, PyPDF2, and Groq Llama 3.1. Users can ask natural language questions, and the assistant answers using the uploaded PDF as the knowledge source.
# 📄 PDF Chatbot using Groq Llama 3.1

An AI-powered PDF Question Answering application that allows users to interact with PDF documents using natural language.

The application extracts text from a PDF file and sends the document context along with the user's question to the Groq Llama 3.1 model, which generates accurate answers based only on the uploaded document.

---

## Features

- Read PDF documents using PyPDF2
- Ask questions in natural language
- AI-powered answers using Groq API
- Restricts responses to PDF content
- Returns "Not in PDF" when information is unavailable
- Simple command-line interface
- Lightweight and beginner-friendly implementation

---

## Tech Stack

- Python
- Groq API
- Llama 3.1 8B Instant
- PyPDF2

---

## Project Structure

```
pdf-chatbot/
│
├── main.py
├── requirements.txt
├── sample.pdf
├── README.md
└── .gitignore
```

---

## Installation

Clone the repository

```bash
git clone https://github.com/yourusername/pdf-chatbot-groq.git
```

Move into the project directory

```bash
cd pdf-chatbot-groq
```

Install dependencies

```bash
pip install -r requirements.txt
```

---

## Requirements

```
groq
PyPDF2
```

or

```bash
pip install groq PyPDF2
```

---

## Configure API Key

Set your Groq API key as an environment variable.

Example (Linux/macOS)

```bash
export GROQ_API_KEY=your_api_key
```

Example (Windows)

```powershell
set GROQ_API_KEY=your_api_key
```

---

## Usage

Place your PDF inside the project folder.

Update the PDF path if needed.

Run

```bash
python main.py
```

Example

```
You: What is Machine Learning?

Bot: Machine Learning is...
```

Type

```
exit
```

to quit.

---

## How It Works

1. Load the PDF
2. Extract text using PyPDF2
3. Accept user questions
4. Build a prompt containing the PDF content
5. Send the prompt to Groq Llama 3.1
6. Display the generated answer

---

## Current Limitation

This implementation sends only the first portion of the extracted PDF text to the language model due to context window limitations. Questions about later sections of large PDFs may not be answered correctly.

Future versions can improve this using Retrieval-Augmented Generation (RAG), embeddings, and vector databases.

---

## Future Improvements

- RAG pipeline
- FAISS vector database
- Sentence Transformers embeddings
- Streamlit web interface
- Multi-PDF support
- Chat history
- PDF highlighting
- Source citations
- OCR support for scanned PDFs
- Docker deployment

---

## Learning Outcomes

- Working with LLM APIs
- Prompt Engineering
- PDF Parsing
- Context-based Question Answering
- Python File Handling
- API Integration

---

## License

MIT License
