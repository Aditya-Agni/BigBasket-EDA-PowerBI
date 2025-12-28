# BigBasket Product Data – Exploratory Data Analysis (EDA)

## Table of Contents
- [Objective](#objective)
- [Project Overview](#project-overview)
- [Python Exploratory Data Analysis](#python-exploratory-data-analysis)
- [Dashboard Preview](#dashboard-preview)
- [Key Insights](#key-insights)
- [Limitations](#limitations)
- [Tools Used](#tools-used)

## 🎯 Objective
The objective of this project is to explore BigBasket’s product catalog to understand how products are distributed across categories, how pricing and discounts vary, and which brands dominate the platform. The analysis aims to simulate a real-world exploratory workflow that supports business decision-making.

---

## 📌 Project Overview
Exploratory Data Analysis of BigBasket product data using Power Query, Power BI, and Python to analyze product distribution, pricing, brand dominance, and discount patterns through dashboards and scripts.

---

## 📂 Dataset
- ~27,000 product records
- Key attributes include:
  - Index 
  - Product name
  - Category & sub-category
  - Brand
  - Sale price & market price
  - Ratings
  - Description
- Each row represents a **unique product listing**

---

## 🧹 Data Cleaning & Preparation (Power Query)
The following steps were performed in **Power Query**:

- Removed unwanted columns (index,description)
- Corrected data types for numeric and categorical columns
- Handled missing values:
  - Filled missing sale prices using market price (assumed no discount)
  - Did not fill missing values in rating because not every product is rated
- Removed true duplicate records
- Standardized text fields (categories, brands)
- Created new features:
  - Discount amount
  - Discount percentage
  - Discount status (Discounted vs Not Discounted)
- Identified and reviewed pricing anomalies
- Created summary tables using Group By for category and brand analysis

---

## Python Exploratory Data Analysis

This project includes a complete Python-based exploratory data analysis notebook (`python/bigbasket_eda_python.ipynb`) that explores:
- Price distribution
- Rating distribution
- Category and brand dominance
- Discount behavior
- Relationships between price, discount, and rating

This demonstrates analytical skills using Python, highlighting patterns not easily shown in dashboards.

---

### Python Notebook
Explore the detailed Python EDA notebook here:
📄 [bigbasket_eda_python.ipynb](python/bigbasket_eda_python.ipynb)

---

## 📊 Dashboard Preview

### Executive Overview
Executive Overview
<img width="1280" height="719" alt="overview_page png" src="https://github.com/user-attachments/assets/98a65b55-57de-4c04-a2e2-97c43c53d734" />


### Category & Discount Analysis
Category & Discount Analysis
<img width="1279" height="722" alt="category_discount_analysis png" src="https://github.com/user-attachments/assets/f1866d17-d8aa-416f-91d8-8b401dbc5367" />

## ▶️ How to Use
1. Download the `.pbix` file from the `dashboard/` folder
2. Open it in Power BI Desktop
3. Review the report pages to explore insights interactively

## 📊 Exploratory Data Analysis
The EDA was structured across **two Power BI report pages**:

### Page 1 – Executive Overview
- Total products, brands, and categories
- Average selling price
- Top brands by product count
- Proportion of discounted vs non-discounted products

### Page 2 – Category & Discount Analysis
- Product count by category
- Average selling price by category
- Average discount by category
- Discount distribution for discounted products only

---

## 🔑 Key Insights
- **Beauty & Hygiene** dominates product listings, making it the most competitive category.
- **Baby Care** has the highest average selling prices, indicating a premium product segment.
- **Kitchen, Garden & Pets** receives the highest average discounts among categories.
- Most product discounts fall between **5%–25%**, while steep discounts above **50%** are rare.
- A small number of brands account for a large share of the product catalog.

---

## ⚠️ Limitations
- The dataset represents product listings, not actual sales transactions.
- Revenue or demand-based conclusions cannot be drawn without quantity sold data.
- Ratings are incomplete, as not all products have been reviewed.

---

## 🛠 Tools Used
- **Power Query** – Data cleaning, transformation, and feature engineering
- **Power BI** – Data visualization and dashboard creation
