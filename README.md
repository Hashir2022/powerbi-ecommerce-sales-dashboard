# 🛒 E-Commerce Sales Dashboard | Power BI

### 📊 Project Overview
This project showcases an **interactive Power BI dashboard** built to analyze and visualize the performance of an e-commerce store.  
The goal is to transform raw sales and customer data into actionable insights for better decision-making.

---

### 🧩 Dataset Details
The project uses two CSV files:
- **orders.csv** → Contains Order ID, Order Date, Customer Name, State, and City  
- **details.csv** → Contains Order ID, Amount, Profit, Quantity, Category, Sub-Category, and Payment Mode  

Both files are connected in Power BI using the `Order ID` field to create a relational data model.

---

### ⚙️ Tools & Technologies
- **Power BI** — Data modeling, DAX measures, and dashboard design  
- **DAX (Data Analysis Expressions)** — Custom calculations for KPIs  
- **Power Query** — Data transformation and cleaning  

---

### 📈 Key Insights & Features
- Total Sales, Profit, and Profit Margin  
- Category & Sub-Category Sales Analysis  
- Regional Sales (State & City)  
- Payment Mode Distribution  
- Year-over-Year (YoY) and Cumulative Growth Metrics  
- Interactive visuals and slicers for dynamic filtering  

---

### 🧮 Sample DAX Measures
```DAX
Total Sales = SUM('details'[Amount])

Total Profit = SUM('details'[Profit])

Profit Margin % = DIVIDE([Total Profit], [Total Sales], 0)

Avg Order Value = DIVIDE([Total Sales], DISTINCTCOUNT('orders'[Order ID]), 0)
