# COVID-19-Testing-Analysis
This project provides an end-to-end exploratory and analytical view of global COVID-19 testing data using Python, SQL, and Power BI. It covers data cleaning, exploratory data analysis (EDA), SQL-based data querying, and dashboard planning for insights such as testing intensity, data completeness, and trends over time.

---

## Phase 1–3: Data Preprocessing & EDA (Python)

The notebook `COVID.ipynb` performs:

- Cleaning and transforming the dataset
- Extracting country names from entity strings
- Aggregating weekly and monthly test trends
- Top 10 countries by total cumulative tests
- Weekly smoothed trend of testing (7-day average)
- Monthly trend comparison for top countries

**Tools Used:**  
`Pandas`, `Matplotlib`, `Seaborn`, `Plotly`

---

## Phase 4: SQL Analytics Layer

The file `Covid.sql` includes SQL queries for deeper analysis, using a table named `covid_testing_cleaned_updated`.

### SQL Queries Included:
- Total tests per country
- Weekly average increase in tests per country
- Top 5 countries with most testing per 1000 population (requires `country_population` join)
- Null-checks: Countries with missing daily test data
- Latest cumulative total per country (using `ROW_NUMBER()`)

**Assumed DB:** MS SQL Server (uses `ROW_NUMBER()` and `TOP`)

---

## Phase 5: Power BI Dashboard (Not Included in Repo)

This project is intended for a Power BI dashboard with the following sections:

| Report Name            | Visuals Included                                                                 |
|------------------------|----------------------------------------------------------------------------------|
| Global Overview        | KPIs, world map, top 10 countries by cumulative tests                           |
| Trend Analysis         | Monthly/weekly line charts, slicers for country                                 |
| Testing per 1000 People| Bar graphs with conditional formatting                                           |
| Data Completeness      | Table showing missing/irregular test records                                    |
| Source Details         | Table of URLs and data source descriptions (optional from dataset 2)            |

---

## Requirements

- Python 3.7+
- Jupyter Notebook
- SQL Server (or compatible RDBMS)
- Power BI Desktop (for dashboard visualization)

---





