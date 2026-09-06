# Customer Demand & Revenue Forecasting Dashboard

End-to-end data analytics project built as part of my portfolio for the Allianz Data Analytics Graduate Programme.

## Project Overview
Analysis of £17.37M in retail transactions across 5,878 customers and 36,900+ orders using Python and Power BI.

## Results
- Forecast accuracy: MAPE 9.91% on 8-week holdout
- Identified 1,646 lost customers representing major re-engagement opportunity
- Loyal segment (15% of customers) drives 60.85% of total revenue
- Q4 revenue spike confirmed — November peaks at £1.16M

## Project Components
- Data cleaning and validation
- Exploratory data analysis and customer behaviour analysis
- Time-series forecasting (Facebook Prophet)
- Customer segmentation (RFM + K-Means clustering)
- Trend and seasonality analysis
- Interactive Power BI dashboard (4 pages)
- Business recommendations report

## Tech Stack
- Python, Pandas, NumPy
- Plotly, Seaborn, Matplotlib
- Scikit-learn, Prophet, Statsmodels
- Power BI

## Dataset
Online Retail II — UCI Machine Learning Repository
https://archive.ics.uci.edu/dataset/502/online+retail+ii

## Repository Structure
demand-forecasting/
├── data/
│   ├── raw/
│   └── processed/
├── notebooks/
│   ├── 01_cleaning.ipynb
│   ├── 02_eda.ipynb
│   ├── 03_forecasting.ipynb
│   ├── 04_segmentation.ipynb
│   └── 05_trends.ipynb
├── dashboard/
│   └── demand_forecasting_dashboard.pbix
├── reports/
│   └── business_recommendations.md
├── requirements.txt
└── README.md

## Author
Arin Lale
MSc Computing (Artificial Intelligence) — Dublin City University