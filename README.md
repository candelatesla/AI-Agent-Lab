🧠 AI-Agent-Lab

A collection of powerful LangGraph- and CrewAI-based intelligent agents.

This repository hosts modular AI agents built using LangGraph, Groq, CrewAI, and modern vector search pipelines. Each agent is designed to perform advanced reasoning, retrieval, and autonomous workflows over structured and unstructured datasets.

🚀 Current Agent: Fundraising Intelligence Agent

The first agent in this collection is a Fundraising Intelligence AI, capable of:

Semantic search across multiple fundraising datasets

Donor pattern analysis

Campaign performance insights

Retrieval-augmented reasoning (RAG)

Multi-step agent workflows via LangGraph

This agent uses:

Groq LLM API (llama-3.3-70b-versatile)

HuggingFace Sentence Transformers for embeddings

Chroma Vector DB for retrieval

LangGraph for multi-node agent workflow

📂 Project Structure

ai-agent-lab/
│
├── fundraising_agent/
│ ├── data/ # downloaded datasets
│ ├── embeddings/ # vectorstore (Chroma)
│ ├── fundraising_intelligence_agent.ipynb
│
├── future_agents/ # placeholder for new LangGraph or CrewAI agents
│
└── README.md

This structure is designed to scale—additional agents can be added in their own folders.

📊 Fundraising Agent Workflow

Dataset ingestion

Embedding + Vector Store Construction

LangGraph Workflow

retrieve node → finds relevant documents

reason node → answers questions using Groq

Query Execution

Example:
“Explain donor patterns in this dataset.”
“Which campaigns resemble successful ones?”

📦 Installation

In Google Colab:

pip install langchain langgraph langchain-groq sentence-transformers chromadb
pip install "langchain-community>=0.2.0"

🧪 Example Questions You Can Ask

What factors most influence campaign success?

Cluster donors based on similar attributes.

Extract insights from the donor network data.

Summarize contact reports for top donors.

Find campaigns similar to those with high social engagement.

🧭 Roadmap
✔️ Current

Fundraising Intelligence Agent (LangGraph + RAG)

🔜 Upcoming

Email Outreach Agent (CrewAI)

Financial Pattern Analysis Agent

Research Agent

Multi-Agent Ecosystem

🤝 Contributing

This project is actively expanding.
Feel free to open issues, request features, or submit PRs.
