# 📊 Superstore Sales Analysis

## 📌 Project Overview
This portfolio project demonstrates an **end-to-end data analysis** using the **Sample Superstore dataset**, showcasing expertise in:

- **MySQL** → Data cleaning, transformation, and querying  
- **Power BI** → Interactive dashboards for actionable insights  
- **Business Analysis** → Identifying sales trends, profitability, and shipping efficiency  

🔹 **Objective:** Demonstrate ability to handle full data pipeline projects — from raw data to business insights.  
🔹 **Files:** SQL scripts, Power BI dashboards, and code. 

---

## 📂 Dataset Information

- **Source:** [Sample Superstore Dataset (Kaggle)](https://www.kaggle.com/)  
- **Rows:** 9,994  
- **Columns:** 21 (e.g., `Order_ID`, `Customer_Name`, `Category`, `Sub_Category`, `Sales`, `Profit`, `Discount`, `Ship_Date`, `Order_Date`)  
- **Description:** Retail superstore order-level data covering **customers, products, sales, discounts, profit, and shipping (2014–2017)**.  

---

## ⚙️ Tools & Technologies

- **MySQL** → Data cleaning, joins, aggregations, and window functions  
- **Power BI** → KPIs with DAX, dashboards with slicers & filters  
- **Excel** → Initial data exploration and preprocessing  

---

## 🛠️ Usage Instructions

### 🔹 MySQL Queries
1. Import dataset into MySQL (table: `superstore`).  
2. Run queries from `sql/superstore_queries.sql` in MySQL Workbench (or any SQL IDE).  

**Sample Query – Total Sales by Category:**  
```sql
SELECT Category, SUM(Sales) AS Total_Sales
FROM superstore
GROUP BY Category
ORDER BY Total_Sales DESC;
```

### 🔹 Power BI Dashboard  
- **Key Features:**  
  - **KPIs** → Total Sales ($190K), Profit ($53K), Quantity (3K), Profit Margin (28%)  
  - **Filters** → Month, Category, Sub-Category  
  - **Visuals** → Map, line chart, bar chart, pie chart, and summary table  

📸 **Dashboard Preview:**  
(https://github.com/hemantgode44/Superstore-sales-analysis/blob/main/Screenshot.png)

---

## 📊 Visualizations

- **Map:** City-wise sales distribution (top cities: Atlantic City, Dover, Alexandria)  
- **Line Chart:** Quantity trends over time (2014–2017)  
- **Bar Chart:** Total Sales by Category (Technology → Phones leads)  
- **Pie Chart:** Orders by Category  
  - Technology: 51.9%  
  - Office Supplies: 27.17%  
  - Furniture: 20.83%  
- **Table:** Metrics by Category (Sales, Orders, Profit, Quantity, Sales per Segment)  

---

## 🔍 Key Insights

- **Sales Distribution** → Technology leads in both **orders (51.9%)** and **sales (~$98.6K)**  
- **Shipping Delays** → Avg. ship delay: **3.4 days**, with Furniture facing the highest delays → 🚚 Opportunity for logistics optimization  
- **Profitability** → *Furniture – Tables* drives strong sales but has weak **profit margins (10%)** due to high **discounts (15%)** → 📉 Recommendation: Review pricing & discount strategy  

---

## 🛠️ Challenges & Solutions

| **Challenge** | **Solution** |
|---------------|--------------|
| Inconsistent date formats in `Order_Date` & `Ship_Date` | Standardized with `STR_TO_DATE` in MySQL |
| Missing values in `Discount` column | Imputed with median discount (per Sub-Category) in Excel |
| Dashboard performance with multiple slicers | Optimized data model relationships & DAX measures |




