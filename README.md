# 📊 Pandas Data Analysis & Visualization Project (Part 1 & Part 2)

## Overview
This repository documents a comprehensive **data analysis and visualization initiative** using Python’s **Pandas** and **Matplotlib** libraries.  
The work is divided into two phases:

- **Part 1 (Exploratory Analysis)**: Large‑scale retail transaction analysis, focusing on household and product insights.  
- **Part 2 (Advanced Analysis)**: Integration of transactions, products, and household demographics, with time‑series and demographic‑based insights to support acquisition decisions.

Together, these projects showcase the ability to handle millions of rows of data, optimize workflows, and deliver actionable insights in a professional, reproducible format.

---

## 📂 Datasets

### 1. Transactions (`project_transactions.csv`)
- **Rows**: ~2,000,000+  
- **Columns**: 11  
  - `household_key` — Household ID  
  - `BASKET_ID` — Transaction ID  
  - `DAY` — Day of purchase  
  - `PRODUCT_ID` — Product identifier  
  - `QUANTITY` — Units purchased  
  - `SALES_VALUE` — Sales value per line item  
  - `STORE_ID` — Store location  
  - `retail_disc` — Retail discount  
  - `week_no` — Week number  
  - `coupon_disc` — Coupon discount  
  - `coupon_match_disc` — Coupon match discount  

### 2. Products (`products.csv`)
- **Rows**: ~92,000  
- **Columns**: 7  
- Includes product identifiers, names, and category details.  
- Shared key: `PRODUCT_ID`.

### 3. Household Demographics (`household_demographics.csv`)
- **Columns**:  
  - `household_key` (shared with transactions)  
  - `age_desc` — Age description  
  - `marital_status` — Marital status  
  - `income_desc` — Income bracket  
  - `homeowner_desc` — Homeownership status  
  - `household_comp_desc` — Household composition  
  - `household_size_desc` — Household size  

---

## 🎯 Objectives

### Part 1: Exploratory Analysis
- **Data ingestion**: Read multiple CSVs into Pandas DataFrames.  
- **Exploration**: Efficient handling of millions of rows, data type optimization, missing value checks.  
- **Column creation**:  
  - `total_discount = retail_disc + coupon_disc`  
  - `percentage_discount = total_discount / SALES_VALUE` (capped between 0 and 1).  
- **Aggregation & statistics**:  
  - Total sales, discounts, overall discount percentage.  
  - Total quantity sold, maximum quantity anomalies.  
- **Household analysis**:  
  - Distribution of household sales.  
  - Top 10 households by sales and quantity.  
  - Ordered bar charts.  
- **Product analysis**:  
  - Top 10 products by sales value.  
  - Discount rates for top products.  
  - Product lookups from `products.csv`.  
  - Identify product with highest single‑row quantity sold.  

### Part 2: Advanced Analysis
- **Data ingestion**: Read transactions, products, and demographics CSVs.  
- **Optimization**: Import only required columns, convert to smallest appropriate data types.  
- **Time‑series analysis**:  
  - Create `date` column from `DAY`.  
  - Plot monthly sales trends.  
  - Compare 2016 vs 2017 monthly sales (line chart).  
  - Plot total sales by day of week.  
- **Demographics analysis**:  
  - Join transactions with demographics (inner join).  
  - Plot sales by age and income description.  
  - Pivot table: mean household sales by age & household composition.  
  - Style pivot table for clarity.  
- **Combined analysis**:  
  - Join products with transactions + demographics.  
  - Pivot by age description and department.  
  - Focus on youngest demographic to assess future spending potential.  
  - Export pivot table to Excel/CSV for stakeholders.  

---

## 📊 Key Insights & Visualizations

- **Part 1**:
  - Overall statistics (sales, discounts, quantities).  
  - Household spending distributions.  
  - Top households and products visualized with bar charts.  

- **Part 2**:
  - Monthly sales trends (2016 vs 2017).  
  - Day‑of‑week sales patterns.  
  - Demographic breakdowns (age, income, household composition).  
  - Department‑level sales by demographic, highlighting young consumer base.  
  - Exported pivot tables for management review.  

---

## 📌 Project Comparison: Part 1 vs Part 2

| **Aspect** | **Part 1: Exploratory Analysis** | **Part 2: Advanced Analysis** |
|------------|----------------------------------|--------------------------------|
| **Datasets Used** | Transactions, Products | Transactions, Products, Household Demographics |
| **Data Volume** | ~2M rows, 11 columns | ~2M rows + demographics (~thousands of households) |
| **Focus** | Household & product insights | Time‑series & demographic insights |
| **Data Preparation** | Type optimization, missing values, new discount columns | Selective column import, type optimization, date conversion |
| **Key Metrics** | Total sales, discounts, quantities, anomalies | Monthly/weekly sales trends, demographic sales distribution |
| **Household Analysis** | Top households by sales & quantity | Household sales grouped by age, income, composition |
| **Product Analysis** | Top products by sales, discount rates, anomalies | Department‑level sales joined with demographics |
| **Visualizations** | Bar charts, distribution plots, KPI dashboards | Line charts, pivot tables, styled demographic dashboards |
| **Deliverables** | Household & product insights, anomaly detection | Time‑series trends, demographic pivot tables, Excel/CSV exports |
| **Business Value** | Identifies high‑value households & products | Assesses customer demographics, future spending potential |

---

## 🛠️ Tools & Libraries
- **Python 3.13**  
- **Pandas** — Data manipulation, aggregation, cleaning.  
- **Matplotlib** — Visualization (bar charts, line charts, distributions, KPI dashboards).  
- **Jupyter Notebook / VS Code** — Interactive development environment.  

---


