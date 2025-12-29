# 📊 Sample Superstore Sales Portfolio
An end-to-end Power BI analysis focused on retail profitability and regional sales performance.

## 🖥️ Dashboard Preview
![Dashboard Preview](dashboard-preview.png)

## 🎯 Project Objective
The goal of this portfolio project is to analyze the "Sample Superstore" dataset to identify profit leaks, top-performing categories, and shipping efficiency.

## 📁 Project Resources
* **Power BI Report:** [Download .pbix File](https://github.com/serena147/Sample-Superstore-PowerBI-Dashboard/raw/main/Power%20BI%20portfolio/Sample_Superstore_Portfolio.pbix)
* **Dataset:** Sample Superstore Excel Dataset

## 🛠️ Skills & Tools
* **Power Query:** Data cleaning, type conversion, and column splitting.
* **DAX Formulas:** Created measures for `Total Profit`, `Profit Margin %`, and `Year-over-Year (YoY) Growth`.
* **Data Modeling:** Built a relationship between Sales, Products, and Regional managers.

## 💡 Business Insights
* **Product Performance:** Identified that "Technology" has the highest profit margin, while "Furniture" (specifically Tables) is underperforming.
* **Geographic Analysis:** The Western region contributes to the highest volume of sales, but the Eastern region shows faster growth.
* **Shipping Impact:** Analyzed how 'Same Day' shipping affects the return rate of items.

## 🧪 Technical Deep Dive: DAX & Data Modeling
To provide actionable business insights, I developed several custom DAX measures to track Superstore performance:

* **Total Sales:** `Total Sales = SUM(Sales[Amount])`
* **Total Profit:** `Total Profit = SUM(Sales[Profit])`
* **Profit Margin %:** `Profit Margin = DIVIDE([Total Profit], [Total Sales], 0)`
* **Year-over-Year (YoY) Growth:** Used `SAMEPERIODLASTYEAR` to compare current performance against previous periods.

### Data Model Architecture
I implemented a **Star Schema** to ensure optimal report performance:
* **Fact Table:** Sales (Orders)
* **Dimension Tables:** Products, Geography (State/Region), and Calendar.
