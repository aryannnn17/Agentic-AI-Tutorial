# LLM Calling

## Concept

This folder demonstrates how to call Large Language Models (LLMs) using different APIs. It shows basic interactions with Google's Gemini API and Groq's API, including how to send prompts, configure parameters like temperature, and handle different response formats.

## What Was Used

- **Google Gemini API**: Used `langchain-google-genai` to interact with Gemini models (gemini-3.1-flash-lite, gemini-2.5-flash)
- **Groq API**: Used `langchain-groq` to interact with Llama models (llama-3.1-8b-instant)
- **LangChain**: Framework for LLM integration
- **Python-dotenv**: For managing API keys from environment variables

## How to Run

1. **Set up environment variables**:
   - Copy `.env.example` to `.env` in the project root
   - Add your API keys:
     ```
     GOOGLE_API_KEY=your_google_api_key
     GROQ_API_KEY=your_groq_api_key
     ```

2. **Install dependencies** (if not already installed):
   ```bash
   uv pip install langchain-google-genai langchain-groq python-dotenv
   ```

3. **Open the notebook**:
   - Open `llm-call.ipynb` in Jupyter or your preferred notebook editor
   - Run the cells sequentially to see different LLM interactions

4. **Examples in the notebook**:
   - Basic question answering with Gemini
   - System prompts and structured messages
   - Temperature parameter effects (deterministic vs creative outputs)
   - Rhyming responses with Groq's Llama model
