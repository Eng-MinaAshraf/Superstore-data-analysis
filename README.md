# 📊 Superstore Sales Analysis using Power BI

## 📌 Overview

This project presents a comprehensive analysis of the **Superstore Sales dataset** using Power BI.
The goal is to extract actionable insights related to sales performance, customer behavior, product trends, and shipping efficiency.

The analysis leverages data modeling, DAX calculations, and interactive dashboards to support data-driven decision-making.

---

## 🎯 Objectives

* Identify top and underperforming regions based on sales and profit
* Analyze product categories and sub-categories performance
* Understand customer segments and their contribution to revenue
* Evaluate the impact of shipping modes on overall business performance

---

## 📂 Dataset Description

* **Dataset Name:** Superstore Sales Dataset
* **Records:** ~9,800 transactions

### Key Fields:

* Order ID
* Order Date / Ship Date
* Customer Name / Segment
* Region / State / City
* Category / Sub-Category / Product Name
* Sales (Revenue)
* Postal Code

---

## 🛠️ Data Preparation

### 📌 Data Modeling

* Model Type: **Star Schema (Flat Model)**
* Main fact table: `Sales`
* Supporting tables: Date, Product, Customer

### Relationships:

* Date → Sales (Order Date)
* Product → Sales (Product ID)
* Customer → Sales (Customer ID)

### ⚙️ Data Cleaning

* Removed redundant columns
* Handled minor missing values
* Standardized categorical fields
* Created time hierarchy (Year, Month, Quarter)
* Built calculated measures using DAX

---

## 📊 Data Analysis

### 🔹 Sales Insights

* **Top Category:** Technology (~37%)
* **Top Region:** West (~32%)
* **Lowest Region:** South (~16.5%)

### 🔹 Customer Insights

* Consumer segment generates highest total sales
* Corporate segment has highest average order value
* Top profitable customers identified

### 🔹 Product Insights

* Top Products: Copiers, Phones, Binding Machines
* Highest Sub-Categories: Phones, Chairs, Storage
* Least Profitable: Fasteners

### 🔹 Shipping Insights

* Standard Class dominates (~60% of orders)
* Same Day shipping used least but linked to high-value orders

### 🔹 Time Insights

* Peak Months: November & December
* Strong growth in Q4
* Sales spikes often occur on Mondays

### 🔹 Geographic Insights

* Top States: California & New York (~48% of total sales)
* Top Cities: New York City, Los Angeles, Seattle
* Sales concentrated in West and East regions

---

## 📈 DAX Measures (Sample)

```id="7x3zqg"
Total Sales = SUM (Sales[Sales])

Total Orders = DISTINCTCOUNT (Sales[Order ID])

Total Customers = DISTINCTCOUNT (Customer[Customer ID])
```

---

## 📊 Visualizations

* Bar Charts → Sales by Region & Category
* Line Charts → Monthly Trends
* Tree Maps → Sub-Category Distribution
* Pie Charts → Customer Segments
* Map Visual → Geographic Sales Distribution

---

## 💡 Key Insights & Recommendations

* Focus on improving performance in Central and South regions
* Optimize low-performing sub-categories (e.g., Tables, Fasteners)
* Leverage high-performing segments (Consumer & Corporate)
* Improve shipping strategy, especially Same Day utilization
* Enhance inventory planning based on seasonal demand

---

## ⚠️ Challenges

* Handling missing values in Postal Codes
* Creating dynamic DAX measures
* Designing dashboards without clutter
* Aligning analysis with business objectives

---

## 🏁 Conclusion

This project demonstrates how Power BI can transform raw data into meaningful business insights.
The analysis supports strategic decisions in sales optimization, customer targeting, and operational efficiency.

---

## 👨‍💻 Author

Full-Stack .NET Developer | Data Analyst

---

## 🚀 Future Improvements

* Add interactive dashboards using Power BI Service
* Integrate real-time data sources
* Apply predictive analytics models
