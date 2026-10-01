# Retail Sales Analytics Dashboard

An end-to-end data analytics project that turns raw retail transaction data into clear business insights. The workflow covers data cleaning in Python, analysis in PostgreSQL, validation in Excel, and an interactive Power BI dashboard.

![Python](https://img.shields.io/badge/Python-Pandas-blue)
![PostgreSQL](https://img.shields.io/badge/Database-PostgreSQL-336791)
![Power BI](https://img.shields.io/badge/Dashboard-Power%20BI-F2C811)
![Excel](https://img.shields.io/badge/Validation-Excel-217346)
![Status](https://img.shields.io/badge/Status-In%20Progress-orange)

---

## Table of Contents

1. [Project Overview](#1-project-overview)
2. [Problem Statement](#2-problem-statement)
3. [Business Questions](#3-business-questions)
4. [Dataset](#4-dataset)
5. [Tools and Technologies](#5-tools-and-technologies)
6. [Project Workflow](#6-project-workflow)
7. [Repository Structure](#7-repository-structure)
8. [Data Cleaning Summary](#8-data-cleaning-summary)
9. [Metric Definitions](#9-metric-definitions)
10. [Key Insights](#10-key-insights)
11. [Recommendations](#11-recommendations)
12. [Dashboard Preview](#12-dashboard-preview)
13. [How to Run This Project](#13-how-to-run-this-project)
14. [Limitations](#14-limitations)
15. [Future Improvements](#15-future-improvements)
16. [Skills Demonstrated](#16-skills-demonstrated)
17. [Author and Contact](#17-author-and-contact)

---

## 1. Project Overview

This project analyses roughly two years of online retail transactions from a UK-based giftware retailer. The goal is to understand how sales are performing, where revenue comes from, and how much the business depends on repeat customers, then to present those findings in a dashboard that a non-technical stakeholder can use.

**In one sentence:** raw, messy transaction data goes in; validated metrics, an interactive dashboard, and actionable recommendations come out.

---

## 2. Problem Statement

### Business context
The retailer sells to both individual customers and wholesale buyers across many countries. It holds a large volume of raw transaction data but has no consolidated view of sales performance. Decisions about stock, marketing spend, and market focus are made without clear visibility into trends, top products, or customer behaviour.

### Objective
Clean and structure the transaction data, calculate reliable sales metrics, and deliver insights and recommendations that help the business make better decisions.

### Scope

| In scope | Out of scope |
|---|---|
| Revenue trends and seasonality | Profit and margin analysis (no cost data available) |
| Product and country performance | Demand forecasting |
| Repeat vs one-time customer behaviour | Predictive customer modelling |
| Data quality assessment and cleaning | |

---

## 3. Business Questions

1. **Trend:** How does revenue change month over month, and is there seasonality?
2. **Products:** Which products generate the most revenue, and how concentrated is that revenue?
3. **Geography:** Which countries contribute most, and which markets are underdeveloped?
4. **Customers:** What share of revenue comes from repeat customers versus one-time customers?
5. **Order value:** What is the average order value, and how does it vary by month and country?
6. **Action:** Based on these findings, what should the business do differently?

---

## 4. Dataset

| Detail | Description |
|---|---|
| Name | Online Retail II |
| Source | UCI Machine Learning Repository (also available on Kaggle) |
| Period | December 2009 to December 2011 |
| Size | Approximately 1 million rows, 8 columns |
| Grain | One row per product line within an invoice |

> The raw data is not stored in this repository because of its size. Download it from the source above and place it in the `data/` folder.

### Column dictionary

| Column | Description |
|---|---|
| `Invoice` | Order number. A leading "C" indicates a cancellation. |
| `StockCode` | Product code. |
| `Description` | Product name. |
| `Quantity` | Units on the line. Negative for returns and cancellations. |
| `InvoiceDate` | Date and time of the transaction. |
| `Price` | Unit price in GBP. |
| `Customer ID` | Customer identifier. |
| `Country` | Customer's country. |

---

## 5. Tools and Technologies

| Purpose | Tool |
|---|---|
| Data cleaning and exploration | Python, Pandas, Jupyter Notebook |
| Database and analysis | PostgreSQL, SQL |
| Validation | Microsoft Excel (pivot tables) |
| Visualisation | Power BI |
| Version control | Git and GitHub |

---

## 6. Project Workflow

| Step | Activity | Output | Status |
|---|---|---|---|
| 1 | Explore and profile the raw data | Data quality findings | Not started |
| 2 | Clean and transform with Pandas | Cleaned dataset, cleaning log | Not started |
| 3 | Design schema and load into PostgreSQL | `schema.sql`, loaded tables | Not started |
| 4 | Analyse with SQL | `analysis_queries.sql` | Not started |
| 5 | Validate key figures in Excel | Reconciliation of SQL vs Excel | Not started |
| 6 | Build the Power BI dashboard | `.pbix` file, screenshots | Not started |
| 7 | Document insights and recommendations | Completed README | Not started |

---

## 7. Repository Structure

```
retail-sales-analytics/
├── README.md                      Project documentation
├── data/                          Raw data (not committed)
├── notebooks/
│   └── 01_cleaning_eda.ipynb      Data profiling and cleaning
├── sql/
│   ├── schema.sql                 Table definitions
│   └── analysis_queries.sql       Analytical queries
├── dashboard/
│   ├── retail_dashboard.pbix      Power BI file
│   └── screenshots/               Dashboard images
└── docs/
    └── data_cleaning_log.md       Every cleaning decision and its impact
```

---

## 8. Data Cleaning Summary

Every cleaning decision is logged with the number of rows affected and the reasoning. Full detail is in [`docs/data_cleaning_log.md`](docs/data_cleaning_log.md).

*To be completed after cleaning.*

| Issue found | Rows affected | Action taken | Reason |
|---|---|---|---|
| Missing Customer IDs | TBD | TBD | TBD |
| Exact duplicate rows | TBD | TBD | TBD |
| Cancelled invoices | TBD | TBD | TBD |
| Zero or negative prices | TBD | TBD | TBD |
| Non-product stock codes | TBD | TBD | TBD |

**Rows before cleaning:** TBD  **Rows after cleaning:** TBD

---

## 9. Metric Definitions

| Metric | Definition |
|---|---|
| Revenue | `Quantity × Price` for valid sales lines (treatment of cancellations: TBD) |
| Total orders | Count of unique valid invoices |
| Unique customers | Count of distinct Customer IDs |
| Average order value (AOV) | Total revenue ÷ total orders |
| Repeat customer | A customer with two or more distinct orders |
| Month-over-month growth | (This month's revenue − last month's revenue) ÷ last month's revenue |
| Cancellation rate | Cancelled invoices ÷ total invoices |

---

## 10. Key Insights

*To be completed after analysis. Each insight should state the finding, the supporting number, and why it matters.*

1. **Revenue trend:** TBD
2. **Product concentration:** TBD
3. **Geographic mix:** TBD
4. **Customer behaviour:** TBD
5. **Order value:** TBD

---

## 11. Recommendations

*To be completed after analysis. Each recommendation should link directly to an insight above.*

| Recommendation | Supporting insight | Expected impact |
|---|---|---|
| TBD | TBD | TBD |

---

## 12. Dashboard Preview

*Screenshots to be added after the dashboard is built.*

The dashboard will include:
- KPI cards: total revenue, orders, customers, average order value
- Monthly revenue trend
- Top products and category breakdown
- Revenue by country
- Repeat vs one-time customer split
- Filters and drill-down by date, country, and product

---

## 13. How to Run This Project

**Prerequisites:** Python 3.9+, Jupyter, PostgreSQL, Power BI Desktop (Windows).

1. **Clone the repository**
   ```bash
   git clone https://github.com/Abhinav-Analyst7/retail-sales-analytics.git
   cd retail-sales-analytics
   ```
2. **Install Python dependencies**
   ```bash
   pip install pandas numpy matplotlib seaborn openpyxl jupyter
   ```
3. **Download the dataset** from the source in Section 4 and save it in `data/`.
4. **Run the cleaning notebook:** open `notebooks/01_cleaning_eda.ipynb` and run all cells to produce the cleaned file.
5. **Load into PostgreSQL:** run `sql/schema.sql`, import the cleaned file, then run `sql/analysis_queries.sql`.
6. **Open the dashboard:** open the `.pbix` file in Power BI Desktop and refresh the data source.

---

## 14. Limitations

- The dataset has no cost data, so profit and margin cannot be analysed.
- Rows without a Customer ID cannot be included in customer-level analysis.
- The data covers a single retailer over two years, so findings may not generalise to other businesses.
- Additional limitations to be added as the analysis develops.

---

## 15. Future Improvements

- Customer segmentation using RFM (Recency, Frequency, Monetary) analysis
- Cohort and retention analysis
- Sales forecasting
- Automating the data refresh pipeline

---

## 16. Skills Demonstrated

- Data cleaning and quality assessment with Pandas
- Relational schema design and analytical SQL (CTEs, window functions, aggregations)
- Cross-validation of results in Excel
- Dashboard design and KPI communication in Power BI
- Translating data into business recommendations
- Version control and project documentation with Git and GitHub

---

## 17. Author and Contact

**Abhinav Awasthi**
B.Tech Computer Science and Engineering (Data Science), Manipal University Jaipur

- GitHub: [Abhinav-Analyst7](https://github.com/Abhinav-Analyst7)
- LinkedIn: [abhinav-awasthi11](https://www.linkedin.com/in/abhinav-awasthi11)
- Email: abhinavawasthi2904@gmail.com
