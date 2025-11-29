# 🧠 AI-Agent-Lab

A collection of powerful LangGraph- and CrewAI-based intelligent agents designed for real-world automation, reasoning, and retrieval tasks.

This repository hosts modular AI agents built using Groq, LangGraph, CrewAI, vector search, and modern LLM orchestration. Each agent runs as a standalone workflow but follows a unified, scalable structure.

---

## 🚀 Current Agents

### 1. Fundraising Intelligence Agent (LangGraph + RAG)

A semantic intelligence system for analyzing fundraising datasets.

**Capabilities**
- Semantic search across donor + campaign datasets
- Donor pattern analysis
- Campaign performance insights
- Retrieval-augmented reasoning (RAG)
- Multi-step LangGraph workflow (retrieve → reason pipeline)

**Tech Stack**
- Groq LLM (`llama-3.3-70b-versatile`)
- HuggingFace Sentence Transformers embeddings
- Chroma vector DB
- LangGraph workflow orchestration

**Workflow**
1. Dataset ingestion
2. Embedding + Vector Store Creation
3. LangGraph Pipeline
   - `retrieve` node → fetches relevant documents
   - `reason` node → Groq-powered analysis
4. Query Execution

**Example Queries**
- "What factors most influence campaign success?"
- "Cluster donors based on similar attributes."
- "Extract insights from the donor network data."
- "Summarize contact reports for top donors."
- "Find campaigns similar to those with high social engagement."

---

### 2. Job Outreach Email Agent (CrewAI + Groq)

An autonomous agent that generates, enriches, and scores hyper-personalized job outreach emails.

**Capabilities**
- Lead data enrichment
- Job description analysis
- Personalized email generation in chosen tone
- Email quality scoring (clarity, tone, personalization, professionalism)
- Full multi-agent pipeline using CrewAI

**Agents Included**

| Agent | Role |
|-------|------|
| **Lead Enrichment Agent** | Fills missing profile data for personalization |
| **Job Analysis Agent** | Extracts responsibilities, qualifications, themes |
| **Email Writer Agent** | Writes tailored outreach emails |
| **Email Quality Agent** | Evaluates and scores generated emails |
| **Email Scoring Agent** | Provides structured scoring output (1–10) |

**Pipeline Workflow**
1. **Lead Enrichment** – Clean + enhance lead profile
2. **JD Analysis** – Extract skills, themes, and hiring signals
3. **Email Writing** – Craft personalized email in chosen tone
4. **Email Scoring** – Assign score + explanation
5. **Final Output** – Structured JSON with email + score

**Supported Tones**
- `formal`
- `friendly`
- `persuasive`
- `conversational`
- `targeted`

---

## 📂 Project Structure
```
ai-agent-lab/
│
├── fundraising_agent/
│   ├── data/                              # Downloaded datasets
│   ├── embeddings/                        # Chroma vectorstore
│   └── fundraising_intelligence_agent.ipynb
│
├── email_outreach_agent/
│   └── job_outreach_pipeline.ipynb        # CrewAI job email workflow
│
└── future_agents/                         # Placeholder for upcoming agents
```

This layout is modular—each new agent lives in its own folder.

---

## 📦 Installation

### In Google Colab:
```bash
pip install groq langchain langgraph sentence-transformers chromadb crewai
pip install "langchain-community>=0.2.0"
```

### For CrewAI tools:
```bash
pip install crewai-tools
```

---

## 📁 Datasets

### Fundraising Intelligence Agent

- **[Fundraising Data](https://www.kaggle.com/datasets/michaelpawlus/fundraising-data)** - Comprehensive fundraising dataset from Kaggle containing donor information, campaign data, and engagement metrics.

### Job Outreach Email Agent

- **[Leads Dataset](https://www.kaggle.com/datasets/rockbottom73/leads-dataset)**
- **[Jobs and Job Description](https://www.kaggle.com/datasets/kshitizregmi/jobs-and-job-description)**
- **[Resume Dataset](https://www.kaggle.com/datasets/gauravduttakiit/resume-dataset)**

**To use these datasets:**
1. Download from Kaggle
2. Place CSV files in the respective agent's directory
3. Run the notebook to process and embed the data

---

## 🧪 Example Use Cases

### Fundraising Intelligence
- Identify donor segments
- Discover patterns in high-performing campaigns
- Summarize donor histories

### Job Outreach Agent
- Generate 100s of personalized job emails
- Score and filter for quality
- Automate outreach campaigns

---

## 🧭 Roadmap

### ✔️ Completed
- Fundraising Intelligence Agent (LangGraph + RAG)
- Job Outreach Email Agent (CrewAI + Groq)

### 🔜 Coming Soon
- Financial Pattern Analysis Agent
- Research & Literature Agent
- Autonomous Multi-Agent Ecosystem
- Full API backend for all agent workflows

---

## 🤝 Contributing

This repository is actively expanding. Feel free to:
- Open issues
- Request new agents
- Contribute enhancements via pull requests

---

## 🔗 Connect

<p align="left">
<a href="https://www.linkedin.com/in/yashdoshi8" target="blank"><img align="center" src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="Yash Doshi" /></a>
<a href="mailto:yash.doshi@tamu.edu"><img align="center" src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
</p>
