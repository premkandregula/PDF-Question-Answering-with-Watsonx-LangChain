# PDF-Question-Answering-with-Watsonx-LangChain


This project is a **Retrieval-Augmented Generation (RAG)** application built with **IBM Watsonx.ai**, **LangChain**, and **Gradio**.  
It allows users to **upload a PDF file** and **ask questions** about its contents. The system retrieves relevant sections from the document and generates accurate answers using a large language model (LLM).  

---

## 🚀 Features
- Upload a **PDF document** and interact with it through natural language queries.  
- Uses **IBM Watsonx.ai LLMs** (`Mixtral-8x7b-instruct-v01`).  
- Embeddings powered by **IBM Slate Embedding** (`ibm/slate-embedding-40m-1`).  
- **Vector database (ChromaDB)** for efficient retrieval.  
- Simple **Gradio web interface** for user interaction.  

---

## 📂 Project Structure
```
qabot.py         # Main application file
README.md        # Project documentation
requirements.txt # Dependencies
```

---

## 🛠️ Installation & Setup

### 1. Clone the repository
```bash
git clone https://github.com/yourusername/qabot.git
cd qabot
```

### 2. Create a virtual environment (recommended)
```bash
python -m venv venv
source venv/bin/activate   # On Linux/Mac
venv\Scripts\activate      # On Windows
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

If you don’t have a `requirements.txt` yet, here are the dependencies:

```bash
ibm-watsonx-ai
langchain
langchain-ibm
chromadb
gradio==2.2.15
pypdf
```

### 4. Configure IBM Watsonx.ai Credentials
- Create a **Watsonx.ai project** in IBM Cloud.  
- Replace the placeholder values in `qabot.py`:
  ```python
  project_id = "your-project-id"
  url = "your-service-url"
  ```
- Ensure your IBM Cloud credentials are available via environment variables or in your project configuration.  

---

## ▶️ Running the App
Run the script:
```bash
python qabot.py
```

By default, the Gradio app will launch on:
```
http://127.0.0.1:7860
```

---

## 💡 Usage
1. Upload a **PDF file**.  
2. Type your question in the text box.  
3. The chatbot will provide answers based on the PDF contents.  

---

## 📊 Tech Stack
- **Backend:** Python, IBM Watsonx.ai, LangChain  
- **Vector Store:** ChromaDB  
- **Frontend:** Gradio  

---

## 🔮 Future Improvements
- Support for multiple PDF uploads.  
- Option to select different LLMs.  
- Save conversation history.  
- Deploy on **Cloud (Heroku, AWS, or IBM Cloud)** for wider accessibility.  

---

## 📜 License
This project is licensed under the **MIT License**.  
