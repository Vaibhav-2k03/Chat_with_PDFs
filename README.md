
# 📄 Chat with PDF using Gemini Pro

Interact with your PDF documents conversationally using Google’s Gemini Pro and LangChain. Upload multiple PDFs, process them into searchable chunks using embeddings, and ask context-specific questions with precise answers—right from your browser!
---

## 🚀 Features

- 🔍 Extracts text from multiple PDF files  
- ✂️ Chunks large documents for better context handling  
- 🧠 Uses **Google Generative AI Embeddings** (`embedding-001`) for vector storage  
- 🤖 Powered by **Gemini Pro** for intelligent question-answering  
- 🗃️ Stores document vectors locally using **FAISS**  
- 💬 Simple and intuitive UI built with **Streamlit**

---

## 🛠️ Tech Stack

- **Python**
- **Streamlit** – UI framework  
- **LangChain** – Chaining logic and QA handling  
- **Google Generative AI API** – For chat and embeddings  
- **PyPDF2** – PDF text extraction  
- **FAISS** – Vector similarity search  

---

## 📦 Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/chat-with-pdf-gemini.git
   cd chat-with-pdf-gemini
   ```

2. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Set up your environment variables**:
   - Create a `.env` file in the root directory.
   - Add your Google API key:
     ```
     GOOGLE_API_KEY=your_google_api_key_here
     ```

---

## ▶️ How to Use

1. **Run the app**:
   ```bash
   streamlit run app.py
   ```

2. **Upload PDFs**:
   - Use the sidebar to upload one or more PDF files.
   - Click **Submit & Process** to process the documents.

3. **Ask Questions**:
   - Enter your question in the input field.
   - The app will provide an answer based on the PDF content.

---

## 🧠 How It Works

1. **PDF Upload** → Extracts raw text using `PyPDF2`.  
2. **Text Splitting** → Uses `RecursiveCharacterTextSplitter` for chunking.  
3. **Embedding & Vector Store** → Chunks are embedded and stored in **FAISS**.  
4. **Question Input** → User asks a question via the UI.  
5. **Semantic Search** → Relevant chunks are retrieved using similarity search.  
6. **Gemini QA Chain** → LangChain uses **Gemini Pro** to generate answers from context.

---

## 📁 Project Structure

```plaintext
├── app.py               # Streamlit app code
├── requirements.txt     # Project dependencies
├── .env                 # API keys (not included in repo)
├── faiss_index/         # Stored vector data
```

---

## 🔐 Environment Variables

| Variable          | Description                         |
|-------------------|-------------------------------------|
| `GOOGLE_API_KEY`  | Your Google Generative AI API Key   |

---

## 💡 Example Questions

After uploading your PDFs, try questions like:
- "Summarize the main points of the uploaded document."
- "What does the document say about data privacy?"
- "List key takeaways from page 5."

---

## 🙌 Acknowledgements

- [Google Generative AI](https://ai.google.dev/)
- [LangChain](https://www.langchain.com/)
- [FAISS by Facebook AI](https://github.com/facebookresearch/faiss)
- [Streamlit](https://streamlit.io/)

---

## 📜 License

MIT License. Feel free to use and modify this project for educational or commercial purposes.
