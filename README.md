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
baselines, and tests that hit real infrastructure instead of mocks.

---

### 🔧 Featured Projects

**[energy-forecasting-mlops](https://github.com/edeszarka/energy-forecasting-mlops)**
24-hour-ahead forecast of Hungary's hourly electricity load with LightGBM on Databricks
(Unity Catalog, MLflow, Asset Bundles, GitHub Actions).
- **4.07% MAPE** vs **8.93%** for a same-hour-last-week baseline, on the same rows of a rolling-origin backtest (latest production run, ~11 months)
- Training, backtest and serving share one point-in-time feature function; perturbation tests confirm later data can't change a feature
- Retraining is triggered by **forecast error** against the naive baseline, not input drift (on load data, drift mostly tracks the seasons); Evidently stays as a diagnostic
- A challenger is promoted only if it beats the baseline in backtest and stays within 2% of the champion's MAPE on the same recent hours; when no approved model can serve, the naive forecast serves and the reason is logged
- Found the ingestion was reading ENTSO-E 15-minute data as hourly, fixed it, and **withdrew my own earlier results** once I found leakage had inflated them
- 398 tests, 95% coverage of the core library · the model started serving in Nov 2026, so live accuracy is still pending

**[health_assistant](https://github.com/edeszarka/health_assistant)**
Dockerized, fully local health-data assistant (FastAPI, Streamlit, PostgreSQL/pgvector, Ollama).
- Facts come from deterministic code: a rule-based lab-report parser (no LLM in extraction) and Python risk calculators; the LLM only phrases answers, and risk questions bypass it
- Bilingual HU/EN retrieval; similarity threshold set from a committed eval (**17/20 relevant**: EN 10/10, HU 7/10; **0/5 off-topic**)
- Chose between three local LLMs with deterministic answer checks; decisions recorded as ADRs
- Found a silent pgvector bug that had left retrieval empty for six months behind mocked tests; added a regression test and real-pgvector CI

---

### 🧰 Stack

**Core:** Python (pandas, NumPy, scikit-learn) · SQL · PySpark
**ML:** LightGBM · classification on imbalanced data · clustering · anomaly detection · SHAP · statistical testing
**MLOps:** Databricks · Delta Lake · MLflow · GitHub Actions
**Apps & LLM:** FastAPI · Streamlit · PostgreSQL/pgvector · Docker · local LLMs (Ollama)

---

<p align="center"><i>Open to Data Scientist roles — Budapest & remote.</i></p>
