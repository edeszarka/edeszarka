<h1 align="center">Hi, I'm Ede Szarka 👋</h1>
<h3 align="center">Data Scientist (9+ yrs) → AI / LLM Engineer</h3>

<p align="center">
Production-grade ML background on Databricks, now building RAG pipelines, multi-agent systems,
and safety-controlled LLM applications.
</p>

<p align="center">
<a href="https://linkedin.com/in/ede-szarka"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white" /></a>
<a href="mailto:szarkaede@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=flat&logo=gmail&logoColor=white" /></a>
<img src="https://img.shields.io/badge/Budapest%2C%20Hungary-000000?style=flat&logo=googlemaps&logoColor=white" />
</p>

---

### About

I spent 9+ years building production ML systems (forecasting, classification, anomaly detection)
across GE, Utopus Insights, and Bosch — mostly on Databricks/PySpark, with a track record of
turning statistically rigorous models into decisions non-technical stakeholders trust. I'm now
applying that foundation to LLM-based, RAG, and agentic systems: vendor LLM API integration
(Gemini, Groq/Llama), FastAPI backends, RBAC + adversarial-testing safety layers, and multi-agent
orchestration.

---

### 🔧 Featured Projects

**[RenovAI 2.0 — Secure Multi-Agent Architecture & Observability Framework](#)**
Multi-agent system for renovation cost intelligence: a gateway with two-tier intent
classification routes queries to 5 specialized handlers over an MCP server (stdio/SSE) and a
FastAPI NL-to-SQL endpoint (Groq / DeepSeek). Layered safety design — RBAC policy checks,
semantic PII/content-safety scanning, and a human-in-the-loop approval gate — validated against
prompt injection, PII extraction, and RAG-poisoning attacks with a self-built 11-case
adversarial test suite. Spec-driven refactor (Gherkin scenarios) built with AI coding agents.
> *repo private — happy to walk through the architecture or share access on request*

**[health_assistant](https://github.com/edeszarka/health_assistant)**
Full-stack, containerized local AI health assistant — FastAPI backend, Streamlit frontend,
hybrid retrieval combining SQL-based health time-series analytics with pgvector semantic search.
Bilingual (HU/EN) RAG pipeline, end-to-end from data ingestion to LLM response generation.
`Python` `FastAPI` `pgvector` `RAG` `Docker`

**[energy-forecasting-mlops](https://github.com/edeszarka/energy-forecasting-mlops)**
Scalable MLOps pipeline forecasting Hungarian hourly electricity load (24h & 168h horizons) with
LightGBM/Prophet on a Delta Lake medallion architecture. Custom GitHub Actions ingestion to work
around environment network restrictions, Optuna time-series CV with leakage-safe gaps, and an
automated weekly champion/challenger retraining framework.
`Python` `Databricks` `Delta Lake` `LightGBM` `Optuna` `GitHub Actions`

---

### 💼 Experience

- **Data Scientist, Bosch Hungary** (2019–2026) — Statistical/ML modules for a manufacturing
  Root Cause Analysis engine (adopted by task force leaders); Balanced Random Forest + SHAP for
  explainable defect prediction; DTW/clustering for failure-mode hypothesis testing.
- **Data Scientist, Utopus Insights** (2018–2019) — Predictive classification models forecasting
  asset failures 10–15 days ahead from SCADA sensor streams.
- **Data Scientist, GE** (2016–2018) — Long-term financial time-series forecasting; NLP over
  industrial gas-turbine error logs.

### 🧰 Tech Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![PySpark](https://img.shields.io/badge/PySpark-E25A1C?style=flat&logo=apachespark&logoColor=white)
![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=flat&logo=databricks&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat&logo=langchain&logoColor=white)
![Gemini](https://img.shields.io/badge/Gemini%20API-8E75B2?style=flat&logo=googlegemini&logoColor=white)
![Groq](https://img.shields.io/badge/Groq-F55036?style=flat&logo=groq&logoColor=white)

**AI/LLM:** RAG pipelines · Multi-agent orchestration · MCP servers · Prompt-based routing · Adversarial/safety testing
**ML/Analytics:** Multi-horizon forecasting · Statistical validation · Model explainability (SHAP) · Anomaly detection

### 🎓 Certifications
Deep Learning Specialization · ML Data Lifecycle in Production · Structuring ML Projects · Sequences, Time Series and Prediction (Coursera)

---

<p align="center"><i>Open to Data Scientist / AI Engineer roles — Budapest & remote.</i></p>
