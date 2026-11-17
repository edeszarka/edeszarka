<h1 align="center">Hi, I'm Ede Szarka 👋</h1>
<h3 align="center">Data Scientist · Time-series forecasting · Statistical ML · MLOps on Databricks</h3>

<p align="center">
<a href="https://linkedin.com/in/ede-szarka"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white" /></a>
<a href="mailto:szarkaede@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=flat&logo=gmail&logoColor=white" /></a>
<img src="https://img.shields.io/badge/Budapest%2C%20Hungary-000000?style=flat&logo=googlemaps&logoColor=white" />
</p>

---

### About

9+ years of predictive modeling and statistically validated analysis in manufacturing and energy
(GE, Utopus Insights, Bosch). I care about results that hold up: point-in-time features, honest
baselines, and tests that hit real infrastructure where mocks would hide bugs.

---

### 🔧 Featured Projects

**[energy-forecasting-mlops](https://github.com/edeszarka/energy-forecasting-mlops)**
24-hour-ahead forecast of Hungary's hourly electricity load with LightGBM, running as scheduled jobs on Databricks
(Delta bronze/silver/gold, Unity Catalog, MLflow, Asset Bundles, GitHub Actions).
- **4.05% MAPE** vs **8.88%** for a same-hour-last-week baseline, on the same rows of a 12-month rolling-origin backtest (current production run)
- First 281 live hours: **3.3%** vs **6.7%** for the baseline on the same hours (a small sample, about two weeks)
- Training, backtest and serving share one point-in-time feature function; perturbation tests confirm later data can't change a feature
- An hourly monitor compares the served model with the naive baseline over 1, 7 and 30 days and sends email alerts
- Besides weekly retraining, retraining is triggered by **forecast error** against the baseline, not input drift (on load data, drift mostly tracks the seasons). The trigger is unit-tested but hasn't needed to fire live yet; Evidently stays as a diagnostic
- A challenger is promoted only if it beats the baseline in backtest and stays within 2% of the champion's MAPE on the same recent hours; when no approved model can serve, the naive forecast serves and the reason is logged
- Found the ingestion was reading ENTSO-E 15-minute data as hourly, fixed it, and withdrew my own earlier results once I found leakage had inflated them
- 400+ tests, ~95% line coverage of the core library

**[health_assistant](https://github.com/edeszarka/health_assistant)**
Dockerized health-data assistant with local LLM and embeddings (FastAPI, Streamlit, PostgreSQL/pgvector, Ollama).
- Facts come from deterministic code: a rule-based lab-report parser (no LLM in extraction) and Python risk calculators; the LLM only phrases answers, and risk questions bypass it
- Bilingual HU/EN retrieval; similarity threshold set from a small committed eval (**17/20 relevant**: EN 10/10, HU 7/10; **0/5 off-topic**)
- Chose between three local LLMs with deterministic answer checks; decisions recorded as ADRs
- Found a silent pgvector bug that had left retrieval empty behind mocked tests; added a regression test and real-pgvector CI

---

### 🧰 Stack

**Core:** Python (pandas, NumPy, scikit-learn) · SQL · PySpark
**ML:** LightGBM · regression & time-series forecasting · classification on imbalanced data · clustering · anomaly detection · SHAP · statistical testing
**MLOps:** Databricks · Delta Lake · MLflow · Evidently · GitHub Actions
**Apps & LLM:** FastAPI · Streamlit · PostgreSQL/pgvector · Docker · local LLMs (Ollama)

---

<p align="center"><i>Open to Data Scientist roles — Budapest & remote.</i></p>
