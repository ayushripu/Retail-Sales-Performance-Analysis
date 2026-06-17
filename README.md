[![Made with Jupyter](https://img.shields.io/badge/Made%20with-Jupyter-orange.svg)](https://jupyter.org/)
[![MySQL](https://img.shields.io/badge/MySQL-8.0-blue.svg)](https://mysql.com/)
[![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-yellow.svg)](https://powerbi.microsoft.com/)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-2.0%2B-green.svg)](https://pandas.pydata.org/)

# 📊 Retail Sales Performance Analysis
   
**End-to-end data analysis project using Python, SQL, Excel, and Power BI to uncover actionable insights from retail sales data.**

---

## 📌 Project Overview

This project demonstrates a complete **data analytics workflow** — from data extraction and cleaning to exploratory analysis and visualization. The goal is to identify key drivers of sales performance and provide data-driven recommendations for business growth.

---

## 🎯 Key Business Questions Answered

- ✅ Which **products** generate the highest revenue?
- ✅ Which **categories** perform best?
- ✅ Which **regions** contribute most to sales?
- ✅ How do **sales trend over time** (monthly)?
- ✅ What is the **sales distribution** across orders?

---

## 🛠️ Tech Stack

| Tool/Library | Purpose |
|--------------|---------|
| **Excel** | Initial data exploration |
| **MySQL** | Database storage & querying |
| **Python (Pandas, NumPy)** | Data cleaning & analysis |
| **Matplotlib** | Data visualization |
| **Power BI** | Interactive dashboard |

---


---

## 🚀 Getting Started

### 1️⃣ Prerequisites

```bash
# Install required Python libraries
pip install pandas numpy mysql-connector-python matplotlib
```

### 2️⃣ Database Setup (MySQL)

CREATE DATABASE SALES_ANALYSIS;
USE SALES_ANALYSIS;

CREATE TABLE sales_data (
    ORDER_ID INT PRIMARY KEY,
    ORDER_DATE DATE,
    PRODUCT VARCHAR(50),
    CATEGORY VARCHAR(50),
    REGION VARCHAR(20),
    QUANTITY INT,
    UNIT_PRICE FLOAT,
    SALES FLOAT
);

### 3️⃣ Connect MySQL to Python

import mysql.connector
import pandas as pd

conn = mysql.connector.connect(
    host='localhost',
    user='root',
    password='your_password',
    database='SALES_ANALYSIS'
)

# Load data into DataFrame
df = pd.read_sql("SELECT * FROM sales_data", conn)

### 4️⃣ Run the Analysis
Open `sales_analysis.ipynb` in Jupyter Notebook and run cells sequentially.

📈 Key Insights

🏆 Product Performance

Product 	Sales (₹)	 Contribution
Laptop	    659,000	     47.4%
Tablet	    197,500	     14.2%
Monitor	    120,000	     8.6%
Printer	    108,500	     7.8%
Chair	    88,000	     6.3%
💡 Laptop alone drives nearly half of total revenue.

📂 Category Analysis
Category	Sales (₹)	Contribution
Electronics	1,165,500	83.76%
Furniture	226,000	    16.24%
💡 Electronics dominates sales — focus marketing efforts here.

🌍 Regional Performance
Region	Sales (₹)
North	491,000
South	430,000
East	251,000
West	219,500
💡 North region is the highest revenue generator.

📅 Monthly Sales Trend
Month	    Sales (₹)
March	    811,500
April	    456,500
February	123,500
💡 Sales peak in March — consider seasonal promotions.

## 🔍 Sample Analysis Code

# Category-wise sales contribution (%)
category_contribution = (df.groupby('CATEGORY')['SALES'].sum() / df['SALES'].sum() * 100).round(2)
print(category_contribution)

# Monthly sales trend
monthly_sales = df.groupby('MONTH')['SALES'].sum()
print(monthly_sales)

📈 Future Improvements
. Add forecasting (time series prediction for next quarter)
. Integrate customer segmentation (RFM analysis)
. Build automated email reports (daily/weekly)
. Add real-time dashboard using Streamlit
. Incorporate profit margin analysis

## 🤝 Connect with Me

**Ayush Kumar**

[![GitHub](https://img.shields.io/badge/GitHub-@ayushripu-black?logo=github)](https://github.com/ayushripu)

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Ayush%20Kumar-blue?logo=linkedin)](https://www.linkedin.com/in/ayush-kr37/)

[![Email](https://img.shields.io/badge/Email-ayushbbu37%40gmail.com-red?logo=gmail)](mailto:ayushbbu37@gmail.com)

⭐ Show Your Support
If you found this project helpful, please give it a ⭐ on GitHub!


