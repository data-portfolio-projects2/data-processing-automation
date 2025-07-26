### 🧪 Pipeline Segments (Local Setup)

Each module handles a specific part of the pipeline:

#### `ingest.py`
*   **Purpose:** Load an existing CSV file (e.g., from Kaggle) into the pipeline.
*   **Stage:** Ingestion
*   **Input:** `input.csv` from `./data` folder
*   **Output:** Raw DataFrame or write to SQLite for persistence

#### `extract.py`
*   **Purpose:** Retrieve supplementary data from a web source (e.g., weather or open API JSON data).
*   **Stage:** Enrichment
*   **Input:** API endpoint
*   **Output:** JSON-formatted data to be merged with ingested data

#### `transform.py`
*   **Purpose:** Clean and transform both ingested and enriched data (handle missing values, type casting, formatting).
*   **Stage:** Transformation
*   **Input:** Merged data (CSV + JSON)
*   **Output:** Cleaned and enriched DataFrame

#### `analyze.py`
*   **Purpose:** Generate descriptive statistics or key insights.
*   **Stage:** Analysis
*   **Input:** Cleaned DataFrame
*   **Output:** Summary stats, flags, KPIs

#### `export.py`
*   **Purpose:** Output final processed data to a formatted `.xlsx` report or insert into SQLite.
*   **Stage:** Output
*   **Input:** Final DataFrame
*   **Output:** Excel file (e.g., `./output/final_report.xlsx`) or database table

#### `main.py`
*   **Purpose:** Pipeline orchestrator – calls all steps in order; optionally supports CLI execution with `argparse`.
*   **Stage:** Automation
*   **Input:** CLI parameters or default behavior
*   **Output:** Full pipeline run with logs or output files
