# 📊 Retail Sales Intelligence System

A complete end-to-end **Business Intelligence (BI) project** that transforms raw retail transactional data into a structured **Star Schema Data Warehouse**, followed by **OLAP analysis and interactive dashboards** using Python, SQL, and Power BI.

---

## 🎯 Project Overview

This project demonstrates a full BI pipeline:

- Data Extraction from raw CSV files
- Data Cleaning & Transformation (ETL)
- Star Schema Data Warehouse Design
- OLAP analytical modeling
- Interactive dashboard development

The goal is to convert operational retail data into meaningful insights for business decision-making.

---

## 🧠 Key Objectives

✔ Design and implement a Star Schema Data Warehouse  
✔ Perform ETL using Python (Pandas)  
✔ Build fact and dimension tables  
✔ Implement OLAP operations (Roll-up, Drill-down, Slice, Dice)  
✔ Develop interactive dashboards for analytics  

---

## 🏗️ Project Architecture

- 📂 raw_data/
  - customers.csv
  - products.csv
  - sales.csv
  - stores.csv
  - staff.csv

- 📂 etl_pipeline/
  - etl_pipeline.ipynb
  - etl_script.py

- 📂 processed_data/
  - fact_sales.csv
  - dim_customer.csv
  - dim_product.csv
  - dim_store.csv
  - dim_staff.csv
  - dim_time.csv

- 📂 data_warehouse/
  - retail_sales_data_warehouse.sql
  - star_schema_diagram.png

- 📂 powerbi/
  - retail_dashboard.pbix
  - dashboard_screenshots/
    - sales_overview.png
    - product_performance.png
    - customer_insights.png

- 📄 README.md

---

## 📁 Dataset Description

### 🔹 Raw Data Sources

- `customers_v2.csv` → Customer demographic information
- `products_v2.csv` → Product catalog and pricing
- `sales_v2.csv` → Transactional sales records
- `stores_v2.csv` → Store locations and regions
- `staff_v2.csv` → Staff details per store

---

## ⚙️ ETL Pipeline (Extract – Transform – Load)

Implemented using Python (Pandas).

### 🔹 Extract
- Load CSV files into DataFrames

### 🔹 Transform
- Standardize column names
- Remove duplicates
- Handle missing values
- Convert data types (dates, integers, decimals)
- Feature engineering:
  - `TotalSales = Quantity × Price`

### 🔹 Load
- Generate structured tables:
  - Fact Table: `fact_sales`
  - Dimension Tables:
    - `dim_customer`
    - `dim_product`
    - `dim_store`
    - `dim_staff`
    - `dim_time`

---

## 🧊 Data Warehouse Design (Star Schema)

The system follows a **Star Schema architecture**:

### ⭐ Fact Table
- `fact_sales`
  - Measures: quantity, price, total sales

### 📌 Dimension Tables
- Customer Dimension (demographics)
- Product Dimension (category, price)
- Store Dimension (location, region)
- Staff Dimension (employee info)
- Time Dimension (year, month, day)

---

## 🔗 OLAP Implementation

The system supports OLAP analytical operations:

### 📈 Roll-up
Aggregation from:
- Day → Month → Year

### 🔽 Drill-down
Detailed breakdown from:
- Year → Month → Day

### 🔍 Slice
Single dimension filtering:
- Region = “North”

### 🔀 Dice
Multi-dimensional filtering:
- Region + Category + Year

---

## 🧠 Tools & Technologies

- Python (Pandas)
- SQL (MySQL Workbench)
- Power BI

---

## 📊 Dashboard Overview

Built using **Microsoft Power BI**:

### 📌 1. Sales Overview Dashboard
- Sales trend over time
- Regional performance analysis
- KPI metrics (Total Sales, Avg Sales per Transaction)

### 📌 2. Product Performance Dashboard
- Top-selling products
- Category-based revenue analysis
- Product ranking insights

### 📌 3. Customer Insights Dashboard
- Sales distribution by gender
- Age group segmentation
- Regional customer behavior

---

## ⚡ Interactive Features

✔ Slicers (Region, Year, Category)  
✔ Drill-down (Time hierarchy)  
✔ Cross-filtering visuals  
✔ Dynamic KPI updates  

---

## 🗄️ Data Warehouse Implementation

- SQL Schema:
```

data_warehouse/retail\_sales\_data\_warehouse.sql
