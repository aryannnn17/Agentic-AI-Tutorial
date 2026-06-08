# Vector Database

## Concept

This folder introduces vector databases and embeddings - a fundamental concept for building AI applications that need to search and retrieve information based on semantic meaning rather than exact keyword matches.

**Key Concepts**:
- **Embeddings**: Converting text into numerical vectors that capture semantic meaning
- **Vector Database**: Specialized database for storing and searching high-dimensional vectors
- **Semantic Search**: Finding similar content based on meaning, not exact words
- **ChromaDB**: Open-source vector database used in this tutorial

## What Was Used

- **ChromaDB**: Open-source vector database for storing and querying embeddings
- **Default Embeddings**: ChromaDB's built-in embedding model (all-MiniLM-L6-v2, 384 dimensions)

## How to Run

1. **Install dependencies** (if not already installed):
   ```bash
   uv pip install chromadb
   ```

2. **Open the notebook**:
   - Open `vector-database.ipynb` in Jupyter
   - Run cells sequentially

3. **The notebook demonstrates**:
   - Creating a ChromaDB client and collection
   - Adding documents with automatic embedding generation
   - Retrieving documents and viewing their embeddings
   - Querying the database with natural language questions
   - Understanding distance scores (lower = more similar)

## Example Queries Demonstrated

- "i love doing a lot of sports" → Returns sports-related documents
- "who won the most number of grand prix" → Returns F1/racing-related documents

## Why This Matters

Vector databases are the foundation for:
- RAG (Retrieval Augmented Generation) systems
- Semantic search in documents
- Recommendation systems
- AI-powered knowledge bases
