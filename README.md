# Business Performance & Operational Analytics Dashboard

> An end-to-end Python data analytics project that cleans operational order data, tracks business KPIs, compares performance across segments, and visualizes actionable insights.

## Table of Contents
- [Overview](#overview)
- [Business Problem](#business-problem)
- [Dataset](#dataset)
- [Tools & Technologies](#tools--technologies)
- [Project Structure](#project-structure)
- [Data Cleaning & Preparation](#data-cleaning--preparation)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Research Questions & Key Findings](#research-questions--key-findings)
- [Dashboard](#dashboard)
- [How to Run This Project](#how-to-run-this-project)
- [Final Recommendations](#final-recommendations)
- [Author & Contact](#author--contact)

## Overview
This project analyzes **1,497 cleaned operational order records** to understand revenue, profitability, returns, delivery efficiency, and customer satisfaction. Python-based data preparation and exploratory analysis produce KPI summaries and visual comparisons by **month, product category, region, and department**.

**Note:** The data is **synthetic** and intended for learning and portfolio demonstration; findings are not real company performance claims.

## Business Problem
Businesses need a clear view of which products, regions, and departments contribute to performance, and where operational issues may require attention. Without consolidated metrics, it is difficult to monitor profitability, returns, and delivery efficiency. This project creates a repeatable analytical workflow to answer these questions.

## Dataset
- **Source:** Synthetic educational operational orders dataset (`data/business_operations_raw.csv`).
- **Raw data:** 1,501 rows and 12 columns.
- **Cleaned data:** 1,497 rows and 15 columns, including calculated fields.
- **Date range:** January 2025 to August 2026.
- **Key columns:** `OrderID`, `OrderDate`, `Region`, `Department`, `ProductCategory`, `UnitsSold`, `Revenue`, `Cost`, `DeliveryDays`, `CustomerSatisfaction`, `Returned`, and `RevenueTarget`.
- **Derived columns:** `Profit`, `ProfitMarginPct`, and `OrderMonth`.

## Tools & Technologies
| Tool | Purpose |
|---|---|
| Python 3 | Analysis and automation |
| Pandas & NumPy | Data cleaning, transformation, and calculations |
| Matplotlib & Seaborn | Charts and dashboard visualizations |
| Jupyter Notebook / Google Colab | Running and documenting the workflow |
| CSV | Input dataset and exported results |

## Project Structure
```text
Business_Performance_Analytics/
├── Business_Performance_Analytics.ipynb
├── README.md
├── Business_Performance_Analytics_Report.pdf
├── requirements.txt
├── data/
│   └── business_operations_raw.csv
├── outputs/
│   ├── business_operations_cleaned.csv
│   ├── business_kpis.csv
│   ├── monthly_performance_summary.csv
│   ├── category_performance_summary.csv
│   ├── regional_performance_summary.csv
│   └── department_performance_summary.csv
└── images/
    └── business_dashboard.png
```
*The tree above is the recommended repository layout. Keep filenames and notebook input paths consistent when uploading.*

## Data Cleaning & Preparation
1. Loaded the raw dataset and inspected column types, missing values, and duplicate records.
2. Removed duplicate/invalid records and prepared a consistent analysis dataset.
3. Calculated **Profit = Revenue − Cost** and **Profit Margin (%) = Profit / Revenue × 100** where revenue is nonzero.
4. Created an order-month field for time-based analysis.
5. Exported the cleaned dataset and reusable summaries as CSV files.

## Exploratory Data Analysis (EDA)
The analysis includes:
- Overall KPIs: total revenue, profit, profit margin, order count, average order value, return rate, delivery days, and customer satisfaction.
- Monthly business performance trends.
- Revenue and profit comparisons by category, region, and department.
- Descriptive review of delivery time and customer satisfaction (not a causal claim).

## Research Questions & Key Findings
| Research question | Finding |
|---|---|
| What is the overall revenue? | **₹17,652,945.51** |
| How profitable are the orders? | **₹6,104,153.40** profit; **34.58%** margin |
| How many orders were analyzed? | **1,497** cleaned orders |
| What is the average order value? | **₹11,792.21** |
| What are the operational indicators? | **6.55%** return rate; **3.81 days** average delivery; **4.13/5** average satisfaction |
| Which category generated the most revenue? | **Electronics** — ₹8,982,933.12 |
| Which region generated the most revenue? | **South** — ₹4,558,331.02 |
| Which category had the lowest profit margin? | **Beauty** — 34.15% |

These are descriptive results calculated from the synthetic project dataset.

## Dashboard
![Business performance analytics dashboard](images/business_dashboard.png)

The dashboard presents business performance through visual comparisons and trend charts. Supporting data tables are available in the `outputs/` directory. A longer discussion is available in `Business_Performance_Analytics_Report.pdf`.

## How to Run This Project
1. Download or clone the repository.
2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn notebook
   ```
3. Open `Business_Performance_Analytics.ipynb` in **Jupyter Notebook** or **Google Colab**.
4. Ensure the dataset path in the notebook matches the uploaded location. For this layout, use `data/business_operations_raw.csv`; in Colab, upload the data folder or adjust the path to the actual file location.
5. Run the cells from top to bottom (**Runtime → Run all** in Colab).
6. Review the visualizations and exported CSV summaries. Depending on the notebook's save paths, new CSVs may be created in the working directory; reference copies are provided in `outputs/`.

## Final Recommendations
- **Track profitability by category:** Review the lower-margin Beauty category and investigate cost or pricing opportunities.
- **Investigate returns:** Break down the return rate by category and region to prioritize quality or fulfillment checks.
- **Review delivery performance:** Monitor delivery times alongside satisfaction, while avoiding assumptions about causation.
- **Monitor KPIs monthly:** Maintain a recurring dashboard for revenue, profit, margins, and operational metrics.
- **Investigate regional differences:** Explore why the South region leads revenue and whether effective practices can transfer to other regions.

**Conclusion:** This project demonstrates a practical Python analytics workflow from raw data to cleaned records, KPI analysis, business visualizations, and evidence-based recommendations. Findings are illustrative because the dataset is synthetic.

## Author & Contact
**Name:** Soumya Ranjan Bhola <br>
**Project:** Business Performance & Operational Analytics Dashboard <br> 
**Email:** soumyaranjan0359@gmail.com <br>
**Linkedin:** www.linkedin.com/in/bsoumyaranjan
