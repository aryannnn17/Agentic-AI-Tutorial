# RAG (Retrieval Augmented Generation)

## Concept

RAG combines the power of vector databases with LLMs to create systems that can answer questions based on custom documents. The process works as follows:

1. **Document Loading**: Load documents (PDF, text, etc.)
2. **Text Splitting**: Split documents into smaller chunks
3. **Embedding**: Convert chunks to vector embeddings
4. **Vector Storage**: Store embeddings in a vector database
5. **Retrieval**: When a question is asked, retrieve relevant chunks
6. **Generation**: Pass retrieved chunks to LLM to generate an answer

This allows LLMs to answer questions about information they weren't trained on, using your own documents.

## What Was Used

- **LangChain**: Framework for building RAG pipelines
- **ChromaDB**: Vector database for storing embeddings
- **HuggingFace Embeddings**: `sentence-transformers/all-MiniLM-L6-v2` model
- **Groq API**: Llama-3.1-8b-instant model via `langchain-groq`
- **PyPDFLoader**: For loading PDF documents
- **RecursiveCharacterTextSplitter**: For intelligent text chunking

## How to Run

1. **Set up environment variables**:
   - Copy `.env.example` to `.env` in the project root
   - Add your Groq API key:
     ```
     GROQ_API_KEY=your_groq_api_key
     ```

2. **Install dependencies** (if not already installed):
   ```bash
   uv pip install langchain langchain-community langchain-huggingface langchain-chroma langchain-groq pypdf sentence-transformers
   ```

3. **Open the notebook**:
   - Open `rag-notebook.ipynb` in Jupyter
   - Run cells sequentially

4. **The notebook demonstrates**:
   - Loading a telecom technical guide PDF
   - Splitting text into chunks (500 characters with 75 overlap)
   - Creating embeddings and storing in ChromaDB
   - Testing retrieval with sample queries
   - Building a complete RAG chain with LangChain
   - Answering questions about the telecom guide

## Sample Queries

- "How does VoLTE work? and what are its benefits?"
- "What is VoWiFi?"
- Any question about mobile networks, VoLTE, security, etc.

## Why RAG Matters

RAG enables:
- Building chatbots for your own documentation
- Reducing hallucinations by grounding answers in facts
- Keeping knowledge up-to-date without retraining models
- Domain-specific AI assistants
