# 🌍 COVID-19 Global Trends Analysis

![Python](https://img.shields.io/badge/Python-3.12-blue)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Database-blue)
![Power BI](https://img.shields.io/badge/PowerBI-Dashboard-yellow)
![Status](https://img.shields.io/badge/Status-In%20Progress-orange)

---

## 📌 Project Overview

This is an end-to-end data analytics project that analyses the global spread of COVID-19 using real-world data from Kaggle. The project covers the full data analytics workflow — from raw data ingestion and cleaning, through to SQL-based analysis and interactive Power BI dashboards.

The goal of this project is to uncover meaningful insights from COVID-19 data and present them in a clear, business-ready format that supports data-driven decision making.

This project was built as part of a personal portfolio to demonstrate practical skills in Python, SQL, data visualisation, and business intelligence reporting.

---

## 🎯 Project Objectives

- Analyse global COVID-19 trends across confirmed cases, deaths, and recoveries
- Identify the top 10 most affected countries by confirmed cases and death rate
- Understand how different WHO regions were impacted
- Track the progression of the pandemic over time using time-series analysis
- Explore the relationship between recovery rate and death rate across countries
- Build an interactive Power BI dashboard for stakeholder-ready reporting

---

## 📂 Dataset

- **Source:** [Kaggle - Corona Virus Report](https://www.kaggle.com/datasets/imdevskp/corona-virus-report)
- **Time Period:** January 2020 – July 2020
- **Files Used:**

| File | Description | Rows |
|------|-------------|------|
| `country_wise_latest.csv` | Latest snapshot of cases per country | 187 |
| `covid_19_clean_complete.csv` | Daily cases by country over time | 49,068 |
| `day_wise.csv` | Global daily totals | 188 |
| `full_grouped.csv` | Country + date grouped data | 35,156 |
| `usa_county_wise.csv` | US county-level data | 627,920 |
| `worldometer_data.csv` | Rich country-level statistics | 209 |

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|------|---------|
| Python (pandas, numpy) | Data loading, cleaning, and manipulation |
| Matplotlib & Seaborn | Data visualisation |
| PostgreSQL | SQL-based data analysis |
| Power BI | Interactive dashboard and reporting |
| GitHub | Version control and project hosting |
| VS Code | Development environment |

---

## 📁 Project Structure

```
covid19-global-analysis/
├── data/
│   ├── raw/               # Original Kaggle CSV files (not pushed to GitHub)
│   └── processed/         # Cleaned datasets ready for analysis
├── notebooks/
│   └── 01_data_loading.ipynb   # Data loading, exploration, cleaning & analysis
├── sql/                   # SQL queries for PostgreSQL analysis
├── powerbi/               # Power BI dashboard files
├── reports/               # Summary reports and exports
└── README.md
```

---

## 🔍 Project Workflow

### Section 1 — Import Libraries
Imported all required Python libraries including pandas, numpy, matplotlib, and seaborn.

### Section 2 — Load Data
Loaded all 6 CSV files into Python using a dictionary-based approach with proper date parsing applied to time-series files.

### Section 3 — Data Exploration
Performed initial data exploration including:
- Head and tail preview of each dataset
- Data types and structure inspection using `info()`
- Statistical summary using `describe()` for both numerical and text columns
- Missing values check
- Duplicate entries check — **0 duplicates found** across all datasets

### Section 4 — Data Cleaning
Addressed all data quality issues found during exploration:
- Filled missing `Province/State` values with `"Unknown"`
- Filled missing `Admin2` (county names) with `"Unknown"`
- Dropped the `FIPS` column from `usa_county_wise` as it was not required for analysis
- Filled missing numerical columns in `worldometer_data` with `0`
- Filled missing text columns in `worldometer_data` with `"Unknown"`
- Saved all cleaned datasets to `data/processed/`

### Section 5 — Analysis & Visualisations
Conducted 6 key analyses with supporting visualisations:

#### 5.1 Global Overview
| Metric | Value |
|--------|-------|
| Total Confirmed Cases | 16,480,485 |
| Total Deaths | 654,036 |
| Total Recovered | 9,468,087 |
| Death Rate | 3.97% |
| Recovery Rate | 57.45% |

#### 5.2 Top 10 Countries by Confirmed Cases
The US accounted for approximately 26% of all global confirmed cases as of July 2020, with 4.3 million cases — more than Brazil and India combined.

#### 5.3 Top 10 Countries by Death Rate
Yemen had an exceptionally high death rate of 28.6%, nearly double that of the United Kingdom at 15.2%. European countries dominated the top 10, reflecting early and severe outbreaks before containment measures took effect.

#### 5.4 Global Trend Over Time
Global confirmed cases grew exponentially from March 2020, reaching 16.4 million by July 2020. Recoveries consistently lagged behind new confirmed cases throughout the period, indicating the pandemic was still accelerating at the dataset's end date.

#### 5.5 Recovery Rate vs Death Rate by Country
European countries showed high death rates with relatively low recovery rates, suggesting cases were still active. Countries in Africa and the Western Pacific achieved higher recovery rates with lower death rates.

#### 5.6 Cases by WHO Region
The Americas accounted for over 50% of global confirmed cases and deaths as of July 2020. Western Pacific regions maintained the lowest case counts, likely due to early containment measures.

---

## 📊 Key Insights

1. **The US was the global epicentre** — accounting for ~26% of all confirmed cases by July 2020
2. **Yemen's death rate of 28.6%** was an extreme outlier, nearly double the next highest country
3. **European countries dominated the death rate rankings** — UK, Belgium, Italy, and France all above 14%
4. **Global cases grew exponentially from March 2020** — the pandemic truly became global in that month
5. **The Americas bore the greatest burden** — highest confirmed cases, deaths, and recoveries across all WHO regions
6. **Recovery rate of 57.45% globally** — meaning ~40% of cases were still active at the dataset's end date

---

## ▶️ How to Run This Project

1. Clone the repository:
```bash
git clone https://github.com/jadliudit/covid19-global-analysis.git
cd covid19-global-analysis
```

2. Install required libraries:
```bash
python -m pip install pandas numpy matplotlib seaborn jupyter ipykernel squarify
```

3. Download the dataset from [Kaggle](https://www.kaggle.com/datasets/imdevskp/corona-virus-report) and place all CSV files in `data/raw/`

4. Open and run the notebook:
```bash
jupyter notebook notebooks/01_data_loading.ipynb
```

---

## 📈 Status

| Section | Status |
|---------|--------|
| Data Loading & Exploration | ✅ Complete |
| Data Cleaning | ✅ Complete |
| Analysis & Visualisations | ✅ Complete |
| SQL Analysis (PostgreSQL) | 🔄 In Progress |
| Power BI Dashboard | 🔄 In Progress |

---

## 👤 Author

**Udit Jadli**
- 📧 jadliudit@gmail.com
- 💼 [LinkedIn](https://www.linkedin.com/in/jadliudit97/)
- 🐙 [GitHub](https://github.com/jadliudit)
- 🌐 [Portfolio](https://job-ready-55.emergent.host/)
