# 🧠 AI-Agent-Lab

A collection of powerful LangGraph- and CrewAI-based intelligent agents designed for real-world automation, reasoning, retrieval, and financial analysis.

This repository hosts modular AI agents built using **Groq**, **LangGraph**, **CrewAI**, and modern LLM orchestration patterns.
Each agent runs as a standalone workflow but follows a unified, scalable structure.

---

## 🚀 Current Agents

---

# **1. Fundraising Intelligence Agent (LangGraph + RAG)**

A semantic intelligence system for analyzing multi-source fundraising datasets.

### **Capabilities**

* Semantic search across donor + campaign datasets
* Donor pattern analysis
* Campaign performance insights
* Retrieval-augmented reasoning (RAG)
* Multi-step LangGraph workflow (retrieve → reason)

### **Tech Stack**

* Groq LLM (`llama-3.3-70b-versatile`)
* HuggingFace Sentence Transformers embeddings
* Chroma vector DB
* LangGraph workflow orchestration

### **Workflow**

1. Dataset ingestion
2. Embedding + Vector Store Creation
3. LangGraph Pipeline
   * `retrieve` node → fetches relevant documents
   * `reason` node → Groq-powered analysis
4. Query Execution

### **Example Queries**

* "What factors most influence campaign success?"
* "Cluster donors based on similar attributes."
* "Extract insights from the donor network data."
* "Summarize contact reports for top donors."
* "Find campaigns similar to high-engagement ones."

---

# **2. Job Outreach Email Agent (CrewAI + Groq)**

An autonomous multi-agent pipeline that enriches lead data, analyzes job descriptions, generates personalized emails, and evaluates them with a scoring model.

### **Capabilities**

* Lead data enrichment
* Job description parsing
* Personalized email generation
* Tone customization
* Email scoring (clarity, tone, personalization, professionalism)
* Full CrewAI multi-agent orchestration

### **Agents Included**

| Agent                     | Role                                               |
| ------------------------- | -------------------------------------------------- |
| **Lead Enrichment Agent** | Fills missing profile data for personalization     |
| **Job Analysis Agent**    | Extracts responsibilities, qualifications, signals |
| **Email Writer Agent**    | Crafts tailored outreach emails                    |
| **Email Quality Agent**   | Scores quality + professionalism                   |
| **Email Scoring Agent**   | Returns structured scoring output (1–10)           |

### **Pipeline Workflow**

1. Lead Enrichment
2. JD Analysis
3. Email Writing
4. Email Scoring
5. Final Output → JSON with `email`, `score`, and `explanation`

### **Supported Tones**

* `formal`
* `friendly`
* `persuasive`
* `conversational`
* `targeted`

### **Tech Stack**

* Groq LLM (`llama-3.3-70b-versatile`)
* CrewAI Multi-Agent Pipeline
* Python, Pandas for dataset handling

---

# **3. Financial Pattern Analysis Agent (LangGraph + Groq)**

*(✨ Newly Added)*

An intelligent agent that analyzes **real + synthetic fundraising financial datasets** to detect patterns, trends, outliers, donor behaviors, and comparative insights.

### **Capabilities**

* Automatic financial column detection
* Descriptive statistical analysis
* Donor + contribution pattern extraction
* Cross-dataset financial comparison
* Outlier detection
* Multi-step LangGraph reasoning pipeline

### **Tech Stack**

* Groq LLM (`llama-3.3-70b-versatile`)
* LangGraph stateful agent workflow
* Pandas for data analysis
* Auto-detection of financial metrics (no Chroma required)

### **Workflow**

1. Load multiple financial datasets (real + synthetic)
2. Detect financial columns (donation amounts, totals, raised amounts)
3. Build combined financial summary
4. LangGraph agent performs structured reasoning

### **Example Queries**

* "What financial patterns do you observe across both datasets?"
* "Which donor segments contribute the most revenue?"
* "Identify outliers in donation amounts."
* "Compare real vs. synthetic donor behavior."
* "What fundraising strategies do the stats suggest?"

---

## 📂 Project Structure
```
ai-agent-lab/
│
├── fundraising_agent/
│   ├── data/
│   ├── embeddings/
│   └── fundraising_intelligence_agent.ipynb
│
├── email_outreach_agent/
│   └── job_outreach_pipeline.ipynb
│
├── financial_pattern_agent/
│   └── financial_pattern_analysis_agent.ipynb
│
└── future_agents/
```

Each agent lives inside its own modular directory.

---

## 📦 Installation

### In Google Colab:
```bash
pip install groq langchain langgraph sentence-transformers chromadb crewai
pip install "langchain-community>=0.2.0"
```

### CrewAI Tools
```bash
pip install crewai-tools
```

---

## 📁 Datasets

### **Fundraising Intelligence Agent**

* Kaggle: **Michael Pawlus – Fundraising Data**
  Comprehensive donor + campaign dataset.

### **Job Outreach Email Agent**

* Leads Dataset
* Jobs and Job Descriptions Dataset
* Resume Dataset

### **Financial Pattern Analysis Agent**

* **Real fundraising dataset** (Michael Pawlus)
* **Synthetic fundraising financial dataset**
* Both loaded automatically based on your folder structure

To use:

1. Download from Kaggle
2. Place inside the respective folders
3. Run notebooks

---

## 🧪 Example Use Cases

### Fundraising Intelligence

* Identify donor segments
* Detect campaign impact drivers
* Run semantic search on donor records

### Job Outreach Email Agent

* Generate highly personalized outreach messages
* Score output emails before sending
* Automate lead → job-email workflow

### Financial Pattern Agent

* Compare synthetic vs real donation patterns
* Detect anomalies in donation behavior
* Summarize entire datasets into insights

---

## 🧭 Roadmap

### ✔️ Completed

* Fundraising Intelligence Agent
* Job Outreach Email Agent
* Financial Pattern Analysis Agent

### 🔜 Coming Soon

* Research & Literature Agent
* Autonomous Multi-Agent Ecosystem
* Full API backend for all agent workflows

---

## 🤝 Contributing

This repository is growing rapidly — feel free to:

* Submit issues
* Request new agents
* Contribute enhancements

---

## 🔗 Connect

<p align="left">
<a href="https://www.linkedin.com/in/yashdoshi8" target="blank"><img align="center" src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="Yash Doshi" /></a>
<a href="mailto:yash.doshi@tamu.edu"><img align="center" src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
</p>

---
