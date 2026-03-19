# DataCo Supply Chain Analytics
### End-to-End Data Analytics Portfolio Project

![Tableau](https://img.shields.io/badge/Tableau-Public-4A7C59?style=flat&logo=tableau)
![Python](https://img.shields.io/badge/Python-3.x-blue?style=flat&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?style=flat&logo=pandas)
![Status](https://img.shields.io/badge/Status-Complete-success)

---

## 📌 Project Overview

This project analyses **180,000+ supply chain orders** from DataCo Global — a large-scale e-commerce operator covering 4 regions, 3 customer segments, and 40+ product categories across global markets.

The goal was to identify revenue drivers, delivery SLA failures, and profitability gaps — and translate raw data into actionable business recommendations using Python and Tableau.

---

## 🔗 Live Dashboards

| Dashboards | Link |
|---|---|
| 📊 DataCo Supply Chain Analytics | [View on Tableau Public](https://public.tableau.com/app/profile/vrushang.gheewala/viz/DataCoSupplyChainAnalytics_17739056561290/SalesRevenueCommandCenter)

---

## 🗂 Dataset

**Source:** [DataCo Smart Supply Chain — Kaggle](https://www.kaggle.com/datasets/shashwatwork/dataco-smart-supply-chain-for-big-data-analysis)

| Property | Detail |
|---|---|
| Rows | 180,519 |
| Columns | 55 |
| Period | 2015 – 2018 |
| Regions | LATAM, Europe, North America, Pacific Asia |
| Format | Single CSV file |

---

## 🛠 Tools & Stack

| Tool | Purpose |
|---|---|
| Python (Pandas, NumPy) | Data cleaning, feature engineering, EDA |
| Matplotlib, Seaborn | Exploratory visualisations |
| Tableau Public | Interactive dashboards |
| Jupyter Notebook | Analysis pipeline |
| Google Sheets | Data documentation |

---

## 📁 Repository Structure

```
dataco-supply-chain/
│
├── DataCoSupplyChainDataset.csv      # Raw dataset (download from Kaggle)
├── supply_chain_master.csv           # Cleaned master CSV → Dashboards 1 & 2
├── segment_profit.csv                # Segment aggregation → Dashboard 3
│
├── supply_chain_analysis.ipynb       # Main Jupyter notebook
│
└── README.md                         # This file
```

---

## 🔬 Jupyter Notebook Pipeline

The notebook covers 10 steps:

1. **Load Raw Data** — `pd.read_csv()` with `latin1` encoding for Spanish characters
2. **Parse Dates** — Convert order/shipping dates, extract month/year/quarter
3. **Calculate Delay** — `delay_days = Days for shipping (real) − Days for shipment (scheduled)`
4. **Flag SLA Breach** — `sla_breach = delay_days > 0`
5. **Clean Order Status** — Flag cancelled, completed, active, and fraud orders
6. **Feature Engineering** — `total_order_value`, `profit_margin_pct`
7. **Segment Grouping** — Group by Customer Segment for profitability analysis
8. **Regional Aggregation** — Group by Country for map visualisations
9. **EDA Charts** — Revenue trends, delay distribution, category analysis
10. **Export CSVs** — `supply_chain_master.csv` + `segment_profit.csv`

---

## 📊 Key Findings

### Dashboard 1 — Sales & Revenue
- **Fishing** is the top category with **$6.9M revenue** and **$756K profit**
- **Standard Class** drives 60%+ of all revenue but has the highest late delivery risk

### Dashboard 2 — Delivery & SLA
- Only **40.8% of orders** are delivered on time — well below the 85% SLA target
- **First Class shipping** has a shocking **95% late delivery rate** — the worst performer
- Over **22,000 orders** are exactly 1 day late — suggesting a systemic scheduling issue

### Dashboard 3 — Customer Segments
- **Consumer segment** generates the most profit at **$2.1M** — nearly double Corporate
- **Top 10 categories** account for the majority of total profit
- **Western Europe** leads globally at **$5.9M** but operates below average margin

---

## 💡 Recommendations

1. **Investigate First Class shipping** — a 95% late delivery rate for a premium tier is unacceptable and likely driving customer churn
2. **Adjust SLA estimates by 1 day** — the largest delay bucket (22K orders) is exactly 1 day late, suggesting a systemic miscalculation
3. **Prioritise logistics investment in Fishing and Cleats categories** — highest profit, most worth protecting
4. **Focus retention efforts on Consumer segment** — highest total profit, most scalable

---

## 👤 Author

**Vrushang Gheewala**
Data Analyst | Operations & Supply Chain

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat&logo=linkedin)](https://www.linkedin.com/in/vrushang-gheewala-350b90291/)
[![Tableau](https://img.shields.io/badge/Tableau-Portfolio-4A7C59?style=flat&logo=tableau)](https://public.tableau.com/app/profile/vrushang.gheewala)

---

## 📄 License

This project uses publicly available data from Kaggle for portfolio and educational purposes.
