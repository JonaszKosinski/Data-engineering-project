# London Bike Usage Analysis

**Research question:** Does temperature and/or public holidays affect daily city bike usage in London?

**Course:** Data Engineering 2025-2026, University of Antwerp  
**Group members:** Jonasz Kosinski, Thijs De Vadder, Lars De Bruyne, Kilian Schober

## Data sources
- `tfl-daily-cycle-hires.xlsx` — Daily TfL bike hire counts (2010–2026), TfL Open Data Portal
- Weather — London daily weather fetched from Open-Meteo historical API (free, no key needed)
- gov.uk Bank Holidays API — UK public holidays from 2019 onwards (JSON)
- Manual backfill — UK bank holidays 2010–2018 compiled from official historical records

## Project structure
- data/raw/ — original data files, never modified
- data/processed/ — cleaned, merged and partitioned files
- notebooks/ — all analysis notebooks, run in order
- report/ — final report

## Notebooks
- 01 data_ingestion — Load TfL Excel, fetch weather and holiday APIs
- 02 cleaning — Remove anomalies, feature engineering
- 03 sql — SQLite database, 7 SQL queries
- 04 spark — PySpark, Spark SQL and DataFrame API
- 05 eda — Exploratory analysis, visualisations, statistical tests
- 06 modelling — Linear Regression and XGBoost, evaluation

## How to run
1. Install dependencies: `pip install -r requirements.txt`
2. Make sure Java is installed (required for Spark) — download from https://adoptium.net
3. Run notebooks in order: 01 → 02 → 03 → 04 → 05 → 06

## Tools used
Python, pandas, PySpark, XGBoost, scikit-learn, matplotlib,
seaborn, SQLite, Parquet, Open-Meteo API, gov.uk API