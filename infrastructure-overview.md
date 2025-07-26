### 🧱 Local-to-Cloud Data Pipeline Mapping

| Pipeline Component | Local Setup | Cloud Setup | Purpose / Notes |
| :--- | :--- | :--- | :--- |
| **Development Environment** | VS Code | GitHub (code + GitHub Actions) | Write, test, and version control your code |
| **Script Orchestration** | Manually run Python scripts in VS Code | GitHub Actions (CI/CD workflows) | Automate ingestion, cleaning, enrichment, and loading |
| **Data Source** | CSV files downloaded from Kaggle | Kaggle API (used in GitHub workflow) | Data source remains the same, access method changes |
| **Staging Area** | Local folder (e.g., `/data/staging/`) | Google Cloud Storage (GCS) bucket | Temporary storage before transformation or loading |
| **Data Transformation** | Python scripts using pandas in VS Code | Python scripts run in GitHub runners | Transform and clean data |
| **Web Data Enrichment** | Python + `requests` or APIs locally | Same logic run via GitHub Actions | Enrich data using APIs like OpenWeatherMap |
| **Data Warehouse / Database**| SQLite or PostgreSQL via DBeaver | BigQuery | Final structured data store |
| **Visualization / Querying**| DBeaver (SQL querying tool) | BigQuery Console / Looker / Data Studio | For analysis or BI dashboards |
| **Environment Management** | `virtualenv` / `pipenv` in local VS Code | GitHub runner uses Python version from workflow | Matches Python environments for consistency |
| **Secrets Management** | `.env` file (locally) | GitHub Secrets | Store API keys and database credentials securely |
| **Monitoring & Logging** | `print()`/logging locally | GitHub Action logs | Debugging and traceability |

---

### 🧭 Summary

Your local setup is a sandbox that mirrors cloud architecture but remains lightweight, offline, and simpler. When you’re confident that the code works:

*   You push to **GitHub**
*   **GitHub** runs the same pipeline
*   **Cloud services** (GCS, BigQuery, APIs) take over automatically

This gives you a reliable, scalable, and maintainable system.
