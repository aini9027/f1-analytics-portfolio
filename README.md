# Formula 1 Race Strategy Analytics
End-to-end data analytics project demonstrating a clean pipeline from data ingestion and SQL analysis to visualization and client-ready reporting.

## Project Goal
Analyze Formula 1 race, qualifying, and lap data to understand how driver performance, team strategy, and pit-stop timing influence race outcomes.

## Objectives
- Ingest and clean historical F1 datasets (Ergast/Kaggle; optional enrichment via FastF1/OpenF1).
- Model a relational schema to support analytical queries.
- Perform SQL-driven exploratory analysis (drivers, constructors, circuits, qualifying vs race).
- Visualize performance and strategy (pit-stop timing, stint pace, circuit effects).
- Produce a concise executive summary for a non-technical audience.

## Repository Structure
```
f1-analytics-portfolio/
├─ data/                     # CSVs/API extracts (not stored in repo)
├─ notebooks/
│   ├─ 01_data_import_and_cleaning.ipynb
│   ├─ 02_exploratory_analysis.ipynb
├─ sql/
│   ├─ schema.sql            # relational model
│   ├─ queries.sql           # analytical SQL
├─ dashboard/                # Power BI / Tableau / Streamlit (placeholder)
├─ reports/
│   ├─ executive_summary.md  # 1-page business insights (template)
├─ .gitignore
├─ requirements.txt
└─ README.md
```

## How to Use
1. Place CSVs from Ergast/Kaggle in `data/` (e.g., `drivers.csv`, `races.csv`, `results.csv`, `lap_times.csv`, `pit_stops.csv`, `qualifying.csv`).
2. Open `notebooks/01_data_import_and_cleaning.ipynb` to create `data/f1.db` (SQLite) and run basic validations.
3. Run the queries in `sql/queries.sql` against `data/f1.db` (or load into PostgreSQL).
4. Build a simple dashboard (Power BI/Tableau/Streamlit) and export screenshots to `reports/`.
5. Summarize findings in `reports/executive_summary.md`.

## Data Sources
- Ergast Motor Racing Data API — historical results, qualifying, pit stops, lap times.
- FastF1 (optional) — timing, telemetry, tyre information for recent seasons.
- Kaggle F1 datasets — convenient CSV mirrors of historical data.

## Author
**Ammar Haider**
