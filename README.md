# Chat with PDF using Gemini 📄🤖

An interactive **Streamlit web app** that allows users to **ask questions from multiple PDF documents**.
The app leverages **Google Gemini** for embeddings and generative AI, combined with **FAISS vector store** for efficient retrieval.
It employs **Retrieval-Augmented Generation (RAG)**, meaning it first retrieves relevant chunks of PDF text before generating answers, improving accuracy and context relevance.

---

## 🚀 Features
* It employs **Retrieval-Augmented Generation (RAG)**
* Upload multiple PDF documents simultaneously
* Convert PDF text into embeddings for semantic search
* Ask natural language questions and receive **context-aware answers** using RAG
* Handles context-based question answering
* Efficient vector search using FAISS

---

## 📦 Installation

Clone the repository:

```bash
git clone https://github.com/Naman919/ASKPDF.git
cd ASKPDF
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Create a `.env` file in the project root and add your **Google API key**:

```env
GOOGLE_API_KEY=your_google_api_key
```

Run the app:

```bash
streamlit run app.py
```
## 🛠️ Tech Stack

| Technology                           | Role                                                 |
| ------------------------------------ | ---------------------------------------------------- |
| Streamlit                            | Web App Interface                                    |
| PyPDF2                               | Extract text from PDF documents                      |
| LangChain                            | Handles text splitting, embeddings, and QA chain     |
| Google Gemini                        | Embeddings and LLM inference                         |
| FAISS                                | Vector store for semantic search                     |
| RAG (Retrieval-Augmented Generation) | Retrieves relevant context before generating answers |
| Python                               | Core development                                     |

---

## 📂 Project Structure

```
/chat-pdf-gemini
├── app.py               # Main Streamlit app
├── requirements.txt      # Python dependencies
├── .env                  # Store your Google API key
├── README.md             # Documentation
```

---

## Workflow

1. **Input PDFs:** Multiple PDFs are loaded and split into document chunks.
2. **Embedding Generation:** Each chunk is converted into embeddings.
3. **Vector Store Ingestion:** Embeddings are stored in FAISS for fast retrieval.
4. **User Query:** A user submits a question via the Streamlit frontend.
5. **Question Embedding:** The query is embedded and matched against the vector store.
6. **Semantic Search and Ranking:** Relevant document chunks are retrieved and ranked.
7. **Answer Generation:** The LLM uses the ranked results to generate an answer.
8. **Output:** The generated answer is displayed in the Streamlit interface.

---

## 🔮 Output

<img width="1822" height="1008" alt="Untitledbbb" src="https://github.com/user-attachments/assets/191b2c90-1624-4bae-b65c-fcf69b5d25bc" />


<img width="1820" height="930" alt="Untitledbbb" src="https://github.com/user-attachments/assets/cd347bfd-1baa-4a3a-9ebe-2876bb107042" />

---

## Future Improvements

* Add **error handling** for invalid PDFs or API failures
* Support **larger PDF files and batch processing**
* Add **multi-user support** for collaborative Q&A
* Export **summary or answer logs** for further analysis

---
