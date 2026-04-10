# London Bike Usage Analysis

**Research question:** Does temperature and/or public holidays 
affect daily city bike usage in London?

**Course:** Data Engineering 2025-2026, University of Antwerp  
**Group members:** ..........

## Data sources
- `tfl-daily-cycle-hires.xlsx` — Daily TfL bike hire counts (2010–2026)
- `UK_holiday.csv` — UK public holidays (2018–2025)
- `weather_london.csv` — London daily weather fetched from 
   Open-Meteo API (free, no key needed)

## Project structure
data/raw/          → original data files, never modified
data/processed/    → cleaned and merged files
notebooks/         → all analysis notebooks, run in order
report/            → final report PDF

## How to run
1. Install dependencies: `pip install -r requirements.txt`
2. Run notebooks in order: 01 → 02 → 03 → 04 → 05

## Tools used
Python, pandas, XGBoost, scikit-learn, statsmodels, 
matplotlib, seaborn, Open-Meteo API