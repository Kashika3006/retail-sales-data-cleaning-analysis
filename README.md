# 🛒 Retail Sales Data Cleaning, Analysis & Power BI Dashboard

## 📌 Project Overview

This project demonstrates an end-to-end data analytics workflow using a retail sales dataset. The objective was to transform raw, messy transactional data into a clean and reliable dataset, perform exploratory data analysis (EDA), validate data quality using business rules, and build an interactive Power BI dashboard for business reporting.

The project highlights practical data analyst skills including data cleaning, data validation, visualization, business insight generation, and dashboard development.

---

## 🛠️ Tools & Technologies

* Python
* Pandas
* NumPy
* Matplotlib
* Power BI
* Git & GitHub

---

## 📂 Dataset

The dataset contains retail transaction records including:

* Transaction ID
* Customer ID
* Product Category
* Product Item
* Quantity Purchased
* Price Per Unit
* Total Spent
* Payment Method
* Purchase Location
* Transaction Date
* Discount Applied

---

## 🧹 Data Cleaning Process

The following cleaning and validation steps were performed:

### Header Standardization

* Converted column names to lowercase
* Replaced spaces with underscores
* Removed formatting inconsistencies

### Missing Value Handling

* Filled missing categorical values with `"Unknown"`
* Imputed missing numerical values using median values
* Calculated missing `total_spent` values where possible

### Data Type Corrections

* Converted quantity to integer format
* Converted transaction dates to datetime format
* Standardized discount status values

### Data Quality Validation

Business rule checked:

```text
Total Spent = Quantity × Price Per Unit
```

Records with imputed pricing information were reviewed separately to avoid false validation failures.

### Outlier Detection

* Used the IQR (Interquartile Range) method on transaction values
* Identified 60 statistical outliers
* Investigated outliers using business logic validation
* Flagged only 4 transactions as potentially inaccurate

### Data Quality Result

* Total Transactions: 12,575
* Valid Transactions: 12,571
* Flagged Transactions: 4
* Data Validity Rate: 99.97%

---

## 📊 Exploratory Data Analysis (EDA)

The analysis focused on understanding sales performance and customer purchasing behavior.

### Revenue Analysis

* Revenue by Category
* Revenue by Location
* Revenue by Payment Method

### Product Analysis

* Top Products by Revenue

### Customer Behavior

* Average Transaction Value
* Discount Impact Analysis

### Time Series Analysis

* Monthly Revenue Trends
* Quarterly Revenue Trends
* Yearly Revenue Trends

---

## 🔍 Key Findings

* Total Revenue generated: **$1.64M**
* Total Transactions analyzed: **12,575**
* Average Transaction Value: **$130.21**
* Revenue was relatively evenly distributed across categories.
* Online sales slightly exceeded in-store sales.
* Discounts had minimal impact on average transaction value.
* Transaction values were positively skewed, with a small number of high-value purchases.
* Only four records required flagging after business-rule validation.

---

## 📈 Power BI Dashboard

An interactive Power BI dashboard was developed using the cleaned dataset.

### Dashboard Features

* Total Revenue 
* Revenue Growth %
* Total Transactions 
* Average Transaction Value 
* Revenue by Category
* Revenue by Location
* Revenue by Payment Method
* Monthly Revenue Trends
* Category Performance Analysis
* Interactive Year Slicer

### Dashboard Preview

<img width="100%" alt="Dashboard Preview" src="powerni/Dashboardscreenshot.png">

---

## 📁 Repository Structure

```text
retail-sales-data-cleaning-analysis/
│
├── data/
│   ├── retail_store_sales.csv
│   └── retail_store_sales_cleaned.csv
│
├── notebooks/
│   ├── data_cleaning.ipynb
│   └── eda.ipynb
│
├── powerbi/
│   ├── retail_sales_dashboard.pbix
│   └── Dashboardscreenshot.png
│
├── README.md
└── requirements.txt
```

---

## 🎯 Skills Demonstrated

* Data Cleaning & Preprocessing
* Data Quality Validation
* Exploratory Data Analysis
* Business Metrics Development
* Data Visualization
* Dashboard Design
* Power BI Reporting
* Git & GitHub Version Control

---

## 🚀 Business Impact

This project demonstrates how raw transactional data can be transformed into actionable business insights through structured cleaning, validation, analysis, and visualization workflows. The resulting dashboard enables stakeholders to monitor revenue performance, understand customer purchasing patterns, and support data-driven decision-making.
