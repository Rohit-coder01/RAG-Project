# 🚀 Retrieval-Augmented Generation (RAG) Application

### Intelligent Document Retrieval & AI-Powered Question Answering using Google Gemini, LangChain, and Pinecone.

A **Retrieval-Augmented Generation (RAG)** project that combines Large Language Models (LLMs) with a vector database to retrieve relevant information from documents and generate context-aware responses.

This application uses **Google Gemini Embeddings** to convert text into vector representations, **Pinecone** to store and retrieve vector embeddings through similarity search, and the **Gemini API** to generate intelligent responses based on the retrieved context.

---

## ✨ Key Features

- 🧠 **Gemini Embeddings:** Converts text and user queries into vector embeddings using Google's `embedding-001` model.
- 🌲 **Pinecone Vector Database:** Efficiently stores, indexes, and retrieves high-dimensional vector embeddings.
- 🔍 **Semantic Search:** Finds contextually relevant document chunks using vector similarity search.
- 🤖 **Gemini-Powered Generation:** Generates natural-language responses using Google's Gemini API.
- 📄 **Document Processing:** Processes documents and prepares their content for retrieval.
- ✂️ **Text Chunking:** Splits documents into smaller chunks to improve retrieval relevance.
- 🔗 **LangChain Integration:** Connects document processing, embeddings, vector storage, and retrieval into a RAG pipeline.
- ⚡ **Context-Aware Responses:** Uses retrieved document context to generate relevant answers.

---

## 🏗️ RAG Architecture

```text
              📄 KNOWLEDGE BASE
               Input Documents
                     |
                     ▼
              Document Loader
                     |
                     ▼
                Text Splitter
                     |
                     ▼
          Google Gemini Embeddings
              (embedding-001)
                     |
                     ▼
              Vector Embeddings
                     |
                     ▼
          🌲 PINECONE VECTOR DATABASE
             (Index: rag-3072)
                     |
              Document Storage
                     |
          ───────────┴───────────

                👤 USER QUERY
                     |
                     ▼
          Google Gemini Embeddings
                     |
                     ▼
             Query Vector
                     |
                     ▼
          🌲 PINECONE SIMILARITY SEARCH
                     |
                     ▼
            Relevant Document Chunks
                     |
                     ▼
             Context Construction
                     |
                     ▼
              Google Gemini LLM
                     |
                     ▼
             💬 AI-GENERATED ANSWER
```

---

## 🛠️ Technology Stack

| Technology | Implementation |
|---|---|
| 🟢 Node.js | Backend Runtime |
| 🔗 LangChain | RAG Pipeline Orchestration |
| 🌲 Pinecone | Managed Vector Database |
| 💎 Google Gemini API | LLM Response Generation |
| 🧠 Gemini `embedding-001` | Text Embedding Generation |
| 🔍 Cosine Similarity | Vector Similarity Search |
| 📦 npm | Dependency Management |
| 🔐 dotenv | Environment Variable Management |

---

## 🌲 Why Pinecone?

**Pinecone** is the central vector database in this project.

Unlike traditional databases that primarily retrieve records through exact matches and structured queries, Pinecone enables semantic retrieval using vector embeddings.

### Pinecone's Role in This Project

- **Vector Storage:** Stores document embeddings along with associated metadata.
- **Indexing:** Organizes vectors for efficient similarity-based retrieval.
- **Semantic Retrieval:** Finds document chunks relevant to a user's query.
- **Similarity Matching:** Uses cosine similarity to identify semantically related vectors.
- **Scalability:** Provides managed vector search infrastructure without requiring self-hosted vector database management.

### Pinecone Configuration

| Parameter | Configuration |
|---|---|
| Vector Database | Pinecone |
| Index Name | `rag-3072` |
| Similarity Metric | Cosine |
| Embedding Provider | Google Gemini |
| Embedding Model | `embedding-001` |

> **Note:** Verify your actual embedding dimensions against your Pinecone index configuration. The legacy `embedding-001` model typically outputs 768-dimensional vectors, whereas an index named `rag-3072` may have been configured for 3072 dimensions. The index name itself does not establish its dimension.

---

## ⚙️ How the RAG Pipeline Works

### 1. Document Ingestion 📄
Documents are loaded into the application to create a searchable knowledge base.

### 2. Text Chunking ✂️
Document content is divided into smaller chunks to make information retrieval more precise and manageable.

### 3. Embedding Generation 🧠
Google Gemini's `embedding-001` model converts document chunks into numerical vector representations.

### 4. Vector Storage in Pinecone 🌲
The generated embeddings are stored in a Pinecone index, making them available for semantic retrieval.

### 5. Query Embedding 🔎
When a user asks a question, the query is converted into a vector using the embedding model.

### 6. Semantic Similarity Search ⚡
Pinecone compares the query vector against stored document vectors using cosine similarity and retrieves the most relevant matches.

### 7. Context-Augmented Generation 🤖
The retrieved document chunks are supplied as contextual information to the Gemini language model.

### 8. Response Generation 💬
Gemini generates a natural-language answer using the retrieved context.

---

## 🚀 Getting Started

### Prerequisites

Before running this project, ensure you have:

- [Node.js](https://nodejs.org/)
- npm
- [Google Gemini API Key](https://aistudio.google.com/apikey)
- [Pinecone Account](https://app.pinecone.io/)

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/Rohit-coder01/RAG-Project.git
```

### 2️⃣ Navigate to the Project Directory

```bash
cd RAG-Project
```

### 3️⃣ Install Dependencies

```bash
npm install
```

### 4️⃣ Configure Environment Variables

Create a `.env` file in the root directory:

```env
GEMINI_API_KEY=your_gemini_api_key
PINECONE_API_KEY=your_pinecone_api_key
PINECONE_INDEX_NAME=rag-3072
```

Add any additional environment variables required by your implementation.

### 5️⃣ Run the Application

```bash
npm start
```

Use the start command defined in your `package.json` if it differs.

---

## 🔐 Security

- Store API credentials in environment variables.
- Never hardcode API keys in source files.
- Add `.env` to `.gitignore`.
- Never commit private credentials to GitHub.

---

## 📚 Core Concepts Demonstrated

- Retrieval-Augmented Generation (RAG)
- Large Language Models (LLMs)
- Text Embeddings
- Vector Databases
- Pinecone Indexing and Vector Search
- Semantic Similarity Search
- Cosine Similarity
- Document Chunking
- Context-Augmented Prompting
- LangChain Integration
- Google Gemini API Integration

---

## 🔮 Future Enhancements

- 📑 Support for multiple document formats (PDF, DOCX, TXT).
- 💬 Conversational memory for multi-turn interactions.
- 🎯 Improved retrieval using advanced chunking strategies.
- 🔍 Metadata filtering and hybrid search.
- 📌 Source attribution and document references.
- 🌐 Interactive web-based chat interface.
- ⚡ Retrieval and response-time optimization.

---

## 👨‍💻 Author

**Rohit Negi**

B.Tech Computer Science Engineering | AI & Machine Learning

- GitHub: [@Rohit-coder01](https://github.com/Rohit-coder01)

---

<div align="center">

### ⭐ If you find this project useful, consider giving it a star!

**Built with ❤️ using Google Gemini, LangChain, and Pinecone.**

</div>
