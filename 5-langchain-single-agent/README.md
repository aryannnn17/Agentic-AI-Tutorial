# LangChain Single Agent

## Concept

This folder demonstrates how to build AI agents using LangChain. An agent is an LLM equipped with tools that can perform specific actions, allowing it to interact with external systems and data.

**Agent Formula**: `Agent = LLM + Tools + Memory`

**Key Concepts**:
- **Tools**: Functions that the agent can call to perform actions (e.g., look up product info, get reviews)
- **System Prompt**: Instructions that define the agent's behavior and role
- **Memory**: Allows the agent to remember context across multiple conversations
- **LangGraph**: Used for creating agents with memory capabilities

## What Was Used

- **LangChain**: Framework for building agents
- **LangGraph**: For agent orchestration and memory management
- **Groq API**: Llama-3.1-8b-instant model via `langchain-groq`
- **InMemorySaver**: For storing conversation history in memory

## How to Run

1. **Set up environment variables**:
   - Copy `.env.example` to `.env` in the project root
   - Add your Groq API key:
     ```
     GROQ_API_KEY=your_groq_api_key
     ```

2. **Install dependencies** (if not already installed):
   ```bash
   uv pip install langchain langchain-groq langgraph
   ```

3. **Open either notebook**:
   - `product-query-agent.ipynb` - Agent without memory
   - `product-query-agent-with-memory.ipynb` - Agent with memory

## Notebook 1: Agent Without Memory

Demonstrates a basic agent that:
- Has access to product information tools
- Can answer questions about products (price, description)
- Can retrieve product reviews
- Does NOT remember context between questions

**Example Issue**: If you ask "Why are people buying Watch?" then "What's the price of this product?", the agent without memory won't know what "this product" refers to.

## Notebook 2: Agent With Memory

Demonstrates an agent with memory that:
- Uses `InMemorySaver` to store conversation history
- Maintains context across multiple questions
- Can reference previous questions in follow-up queries
- Uses thread IDs to manage different user sessions

**Example**: Ask "Why are people buying Watch?" then "What's the price of this product?" - the agent with memory correctly identifies "this product" refers to the Watch.

## Tools Demonstrated

- `get_product_info`: Look up product details (name, price, description)
- `get_product_reviews`: Get product ratings and review counts

## Why Agents Matter

Agents enable:
- Building AI assistants that can perform actions
- Connecting LLMs to databases, APIs, and external systems
- Creating conversational interfaces for complex tasks
- Multi-step reasoning and tool use
