# 📊 Pandas Data Analysis & Visualization Project (P1)

## Overview
This project is a **midcourse data analysis and visualization exercise** using Python’s **Pandas** and **Matplotlib** libraries.  
The analysis is based on large-scale retail transaction data provided as part of a due diligence process for a potential acquisition by **Maven MegaMart**.  
The goal is to explore millions of rows of transactional data, derive meaningful insights, and present them in a clear, professional dashboard-style format.

---

## 📂 Datasets

### 1. Transactions Dataset (`project_transactions.csv`)
- **Rows**: ~2,000,000+
- **Columns**:
  - `household_key`: Household ID
  - `BASKET_ID`: Transaction ID
  - `DAY`: Day of purchase
  - `PRODUCT_ID`: Product identifier
  - `QUANTITY`: Units purchased
  - `SALES_VALUE`: Total sales value per line item
  - `STORE_ID`: Store location
  - `retail_disc`: Retail discount
  - `week_no`: Week number
  - `coupon_disc`: Coupon discount
  - `coupon_match_disc`: Coupon match discount

### 2. Products Dataset (`products.csv`)
- **Rows**: ~92,000
- **Columns**: 7
  - Includes product identifiers, names, and category details.

---

## 🎯 Objectives
- **Data ingestion**: Read multiple CSV files into Pandas DataFrames.
- **Exploration**: Handle millions of rows efficiently, optimize data types, and check for missing values.
- **Column creation**:
  - `total_discount = retail_disc + coupon_disc`
  - `percentage_discount = total_discount / SALES_VALUE`
    - Capped between 0 and 1.
- **Aggregation & statistics**:
  - Total sales, total discounts, overall discount percentage.
  - Total quantity sold, maximum quantity in a single row.
  - Household-level and basket-level sales summaries.
- **Household analysis**:
  - Distribution of household sales.
  - Top 10 households by sales and quantity.
  - Ordered bar charts for top households.
- **Product analysis**:
  - Top 10 products by sales value.
  - Discount rates for top products.
  - Lookup product names from `products.csv`.
  - Identify product with highest single-row quantity sold.

---

## 📊 Key Insights & Visualizations
- **Overall Statistics**:
  - Total sales, discounts, and quantities.
  - Max quantity anomalies flagged for review.
- **Household Analysis**:
  - Distribution plots of household spending.
  - Bar charts of top households by sales and quantity.
- **Product Analysis**:
  - Horizontal bar charts of top-selling products.
  - Discount comparison for top products.
  - Product lookups for anomalies and high-volume items.

---

## 🛠️ Tools & Libraries
- **Python 3.13**
- **Pandas**: Data manipulation, aggregation, and cleaning.
- **Matplotlib**: Visualization (bar charts, distribution plots, KPI dashboards).
- **Jupyter Notebook / VS Code**: Interactive development environment.

---

## 🚀 How to Run
1. Clone the repository:
   ```bash
   git clone git@github.com:Egitto-Data/pandas-data-analysis-visualization-P1.git
