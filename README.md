# Superstore Retail Sales — End-to-End Data Analysis

A single end-to-end Jupyter notebook demonstrating the full analyst workflow: raw CSV → data cleaning → exploratory analysis → SQL → visualization → business recommendations. Built on a real, publicly available retail transactions dataset (8,399 orders from a Canadian office-supply retailer).

## What's in this repo

| File | Description |
|---|---|
| `Superstore_EndToEnd_Analysis.ipynb` | The full analysis — data audit, pandas cleaning, EDA, SQL queries (incl. window functions), 4 visualizations, and business recommendations. Fully executed with outputs visible. |
| `superstore_raw.csv` | The raw, unmodified source data, included so the notebook is fully reproducible. |

## Tools Used

- **Python (pandas, NumPy)** — data cleaning and feature engineering
- **SQLite / SQL** — relational analysis, including CTEs and window functions (LAG, RANK)
- **Matplotlib / Seaborn** — visualization
- **Jupyter Notebook** — end-to-end workflow, documented step by step

## Workflow

1. **Load the raw data** exactly as downloaded — no pre-cleaning
2. **Audit data quality** — find missing values, unparsed dates, and other real issues before touching anything
3. **Clean & engineer features** — parse dates, impute missing values by sub-category, derive profit margin %, shipping days, and more
4. **Exploratory analysis** — distributions and a correlation heatmap to surface early signals
5. **Load into SQLite** and answer 5 business questions with SQL
6. **Visualize** the findings
7. **Translate findings into recommendations**

## Key Findings

- **~19% of order lines are sold at a loss** — the single biggest signal in the dataset.
- **Profit margin declines steadily as discount rate increases**, turning negative at 20%+ discounts.
- **Furniture** is the weakest product category; **Tables** and **Bookcases** are the two least profitable sub-categories, losing money in aggregate.
- **Technology** is the strongest category by total profit.
- Monthly sales show meaningful volatility, suggesting a seasonal pattern worth a deeper look.

## Data Source

Public "Superstore Sales" practice dataset (order-level transactions, Canadian office-supply retailer).
