# E-Commerce Sales Analysis (2010–2011)

Comprehensive e-commerce analytics project using Python. Covering data cleaning, feature engineering, revenue trends, customer behavior, product performance, and return analysis. Built to showcase strong data analysis skills through clean notebooks, reproducible code, and clear business insights.


## 📌 Project Overview

This project analyzes a real e-commerce dataset originally published by the UCI Machine Learning Repository.  
It contains actual retail transactions from 2010–2011 for a UK-based online store that sells all-occasion gifts.

### 📂 Dataset Source
The dataset is widely referenced on Kaggle under the name **Online Retail Dataset**.  
It was originally collected and published by:

**Dr. Daqing Chen  
Director – Public Analytics Group  
London South Bank University, UK**

### 🎯 Objectives
- Clean and preprocess raw retail transaction data  
- Engineer features to enable deeper analysis  
- Explore sales trends, customer behavior, and product patterns  
- Identify return/cancellation behavior  
- Build clear, professional visualizations  
- Produce a polished PDF insights report

--- 

## 📁 Repository Structure
```
Ecommerce-Sales-Analysis/
│
├── data/
│ └── data.rar
│
├── notebooks/
│ ├── 01_Data_Cleaning.ipynb
│ ├── 02_Feature_Engineering.ipynb
│ └── 03_Analysis_and_Visualizations.ipynb
│
├── charts/ 
│ ├── monthly_revenue.png
│ ├── daily_sales.png
│ ├── hourly_sales.png
│ ├── top_products.png
│ ├── top_returns.png
│ ├── country_returns.png
│ └── ...
│
├── report/
│ └── Ecommerce_Sales_Analysis_2010_2011.pdf
│
├── requirements.txt
│
└── README.md
```
---

## 🧹 1. Data Cleaning

Major cleaning steps performed in `01_Data_Cleaning.ipynb`:

- Converted `InvoiceDate` to proper datetime
- Filled missing product descriptions (`Unknown` → replaced with `StockCode`)
- Dropped duplicates
- Standardized text fields
- Handled missing `CustomerID` (kept but interpreted carefully)
- Kept negative quantities to identify returns
- Exported `cleaned_data.csv` (stored inside `data.rar`)


## 🛠️ 2. Feature Engineering

Implemented in `02_Feature_Engineering.ipynb`:

- `net_sales` = Quantity × UnitPrice  
- `is_return` = flag for negative quantities  
- `is_cancelled` = InvoiceNo starting with “C”  
- Extracted:
  - `invoice_month`
  - `invoice_year`
  - `invoice_day`
  - `invoice_hour`

Exported as `featured_data.csv` (inside `data.rar`).


## 📊 3. Analysis & Insights

All analysis and visualizations are inside `03_Analysis_and_Visualizations.ipynb`.

### 🔹 Revenue Trends
- Strong upward trend leading to **November 2011**
- Sudden crash in **December 2011**
- Seasonal spike likely due to pre-holiday shopping

### 🔹 Daily Sales Pattern
- **Thursday** = highest sales  
- **Sunday** = lowest activity

### 🔹 Hourly Activity
- Peak revenue at **12 PM**  
- Slowest at **8 PM**

### 🔹 Top-Selling Products
Stock codes dominating by units sold:
- 22197  
- 84077  
- 85099B  
- 85123A  
- 84879  

### 🔹 Highest Revenue Products
Product categories with consistently high order value and volume.

### 🔹 Returns & Cancellations
- **Return rate:** ~40.88%  
- **Cancellation rate:** ~35.72%  
- USA, Malta, and Japan show highest return ratios.

### 🔹 Customer Analysis
Top customers generate high revenue via bulk purchases.  
Avg order value varies massively across customers.

--- 

## 📈 Visualizations

All key plots are exported into the `charts/` folder:
- Monthly Revenue Trend  
- Daily Sales Pattern  
- Hourly Sales Pattern  
- Top Selling Products  
- Return Frequency by Product  
- Return Percentage by Country  


## 📑 Report

A polished PDF containing:
- Summary of methods  
- Visualizations  
- Key findings  
- Business insights & recommendations  

## 🧪 Requirements

Install dependencies using: 
``` 
pip install -r requirements.txt
```


## 🙌 Acknowledgements

Dataset provided by:  
UCI Machine Learning Repository  
Dr. Daqing Chen — London South Bank University


## 📎 Notes

The `data/` directory contains a single compressed archive (`data.rar`).  
It includes:  
- Raw dataset  
- Cleaned dataset  
- Feature-engineered dataset  

CSV files are compressed to keep the repository size efficient.




