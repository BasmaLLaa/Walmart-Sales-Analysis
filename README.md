# Walmart Retail Sales — Time Series Trend Analysis & Forecasting

This project explores Walmart's historical weekly retail sales data to identify key trends, seasonal patterns, and variation in sales across departments and stores over time. Monthly sales were analyzed using time-series techniques such as moving averages and seasonal decomposition, and two simple forecasting methods — rolling mean and exponential smoothing — were built and evaluated to estimate future sales.

## Dataset

- **421,570** weekly sales records
- **45** stores, **81** departments
- Date range: **February 2010 – October 2012**
- Columns: `Store`, `Dept`, `Date`, `Weekly_Sales`, `IsHoliday`

## Project Workflow

```
Raw Weekly Sales
      ↓
Data Cleaning & Date Conversion
      ↓
Feature Engineering (Year, Month, Quarter)
      ↓
Aggregate Weekly → Monthly
      ↓
      ├── Trend Analysis
      ├── Moving Averages (3-month, 6-month)
      ├── Seasonal Analysis (monthly pattern, year × month heatmap)
      ├── Department Analysis
      ├── Store Analysis
      ├── Year-over-Year Analysis
      └── Holiday Analysis
             ↓
      Forecasting
      ├── Rolling Mean
      └── Exponential Smoothing
             ↓
      Model Evaluation (MAE, RMSE)
             ↓
      Business Insights
```

## Key Findings

| Insight | Result |
|---|---|
| Best-performing month | **December** |
| Weakest month | **January** |
| Top department by total sales | **Dept 92** (~$483.9M) |
| Top store by total sales | **Store 20** (~$301.4M) |

## Forecasting Results

Two forecasting approaches were built on a train/test split of the monthly aggregated series and compared:

| Model | MAE | RMSE |
|---|---|---|
| **3-Month Rolling Mean** | 24,084,560 | 25,352,435 |
| Exponential Smoothing | 30,498,311 | 36,250,357 |

The rolling mean approach outperformed exponential smoothing on this series, producing lower error on both metrics.

## Tech Stack

- **Python** — Pandas, NumPy
- **Matplotlib** — visualization
- **statsmodels** — exponential smoothing
- **scikit-learn** — MAE / RMSE evaluation

## Business Value

Understanding seasonal sales patterns and department/store-level performance supports better inventory planning, staffing, and demand forecasting — helping the business anticipate high-demand periods (e.g., December) and manage low-demand periods (e.g., January) more effectively.

---
*Author: Basmala Elhabshy*
