# 📊 Retail Sales Analytics Dashboard — Power BI Project

## 📌 Project Overview

This project is a fully interactive **Sales Analytics Dashboard** built using **Power BI Desktop**. It transforms raw retail sales data into clear, actionable business insights through dynamic charts, KPI cards, and interactive filters.

The dashboard is designed to help business owners, managers, and analysts quickly understand:
- How much revenue is being generated
- Which products and categories are performing best
- How sales are trending over time
- Which regions and customers are driving the most value

Rather than spending hours going through spreadsheets, this dashboard lets anyone explore the data visually in seconds by clicking, filtering, and drilling down into the details.

---

## 🎯 Project Objectives

| # | Objective | Description |
|---|---|---|
| 1 | Sales Performance Monitoring | Track total revenue, profit, and orders at a glance |
| 2 | Product Analysis | Identify best-selling and low-performing products |
| 3 | Regional Insights | Understand which locations generate the most sales |
| 4 | Customer Behavior | Analyze how customers shop and who spends the most |
| 5 | Trend Analysis | Compare monthly and yearly performance to spot patterns |
| 6 | Business Decision Support | Provide data-backed answers to key business questions |

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| **Power BI Desktop** | Main tool for building the dashboard and visuals |
| **Power Query** | Used to clean, reshape, and transform the raw data before loading |
| **DAX (Data Analysis Expressions)** | Used to write custom calculations and KPI measures |
| **Excel / CSV** | Source file containing the raw sales dataset |

---

## 📂 Project File

| File | Description |
|---|---|
| `DASH_BOARD_-1.pbix` | Main Power BI project file containing the complete data model, all transformations, DAX measures, and the interactive dashboard |

> To open this file, you need **Power BI Desktop** installed. It is free to download from [Microsoft's official website](https://powerbi.microsoft.com/desktop).

---

## 📊 Dashboard Features

### ✅ KPI Cards (Key Performance Indicators)
KPI cards are placed at the top of the dashboard to give an instant snapshot of the most important numbers:

- **Total Sales** — Overall revenue generated across all transactions
- **Total Profit** — Net profit after deducting cost of goods sold
- **Total Orders** — Number of transactions completed
- **Average Sales** — Average revenue per transaction
- **Revenue Growth** — Percentage increase or decrease compared to a previous period

> These cards update dynamically when any filter or slicer is applied, so the numbers always reflect the currently selected view.

---

### 📈 Sales Trend Analysis
A line or area chart that shows how sales have changed over time.

- Displays **monthly and yearly** sales patterns
- Helps identify **peak seasons** and **slow periods**
- Reveals whether the business is growing, declining, or staying flat
- Useful for **forecasting** future performance based on historical trends

---

### 🛒 Product Performance Analysis
Breaks down sales at the product and category level:

- Shows **top-selling products** by revenue and quantity
- Highlights **underperforming products** that may need attention
- Groups products by **category** (e.g. Clothing, Electronics, Beauty)
- Displays each product's **contribution percentage** to total revenue

> This helps businesses decide what to stock more of, what to promote, and what to potentially discontinue.

---

### 🌍 Regional Sales Analysis
Visualizes sales distribution across different geographic locations:

- **Map or bar chart** showing sales by region or city
- Compares **profit margins** across locations
- Identifies the **most and least profitable regions**
- Supports decisions around **market expansion** or resource allocation

---

### 👥 Customer Insights
Analyzes customer purchasing behavior:

- Identifies **top customers** by total spending
- Shows **repeat purchase patterns**
- Segments customers based on buying frequency and value
- Helps in designing **loyalty programs** and **targeted campaigns**

---

### 🎯 Interactive Components
The dashboard is fully interactive — users are not limited to a static view:

| Component | Description |
|---|---|
| **Slicers** | Filter data by date range, category, region, or gender |
| **Drill-down** | Click on a chart to go deeper into the data (e.g. year → month → day) |
| **Cross-filtering** | Clicking one visual automatically updates all other visuals on the page |
| **Dynamic Charts** | All charts respond in real-time to filter selections |

---

## 🔄 Data Processing Workflow

The data went through a structured pipeline before being visualized:

### Step 1 — Data Collection
Raw sales data was collected from a structured Excel/CSV dataset containing transaction records.

### Step 2 — Data Cleaning (Power Query)
The raw data was cleaned inside Power Query Editor:
- Removed duplicate rows
- Handled missing/null values
- Corrected wrong data types (e.g. dates stored as text)
- Standardized column names and formats
- Removed irrelevant columns

### Step 3 — Data Transformation (Power Query)
After cleaning, the data was transformed to make it analysis-ready:
- Created new calculated columns (e.g. Month Name, Year, Profit Margin)
- Merged related tables where needed
- Built relationships between tables in the data model
- Structured the model using a **Star Schema** approach

### Step 4 — DAX Measures
Custom calculations were written using DAX to power KPI cards and advanced visuals:
```
Total Sales = SUM(retail_sales[total_sale])
Total Profit = SUM(retail_sales[total_sale]) - SUM(retail_sales[cogs])
Total Orders = COUNT(retail_sales[transactions_id])
Avg Sale = AVERAGE(retail_sales[total_sale])
Profit Margin % = DIVIDE([Total Profit], [Total Sales], 0) * 100
```

### Step 5 — Dashboard Design
Visuals were arranged into a clean, easy-to-read layout:
- Bar Charts, Line Charts, Pie/Donut Charts
- KPI Cards, Tables, Maps
- Slicers and Filters for interactivity

---

## 💡 Business Questions Answered

This dashboard directly answers the following real-world business questions:

| Question | Visual Used |
|---|---|
| What is our total revenue and profit? | KPI Cards |
| Which products sell the most? | Bar Chart — Product Analysis |
| Which month had the highest sales? | Line Chart — Sales Trend |
| Which region generates the most revenue? | Map / Regional Bar Chart |
| Who are our top 5 customers? | Table — Customer Insights |
| How is sales growth trending year over year? | Line Chart — Yearly Trend |
| Which category contributes the most to revenue? | Pie/Donut Chart |

---

## ▶️ How to Open & Use the Dashboard

### Step 1 — Download Power BI Desktop
If you don't have it installed, download it for free:
👉 [https://powerbi.microsoft.com/desktop](https://powerbi.microsoft.com/desktop)

### Step 2 — Download the Project File
Download `DASH_BOARD_-1.pbix` from this repository.

### Step 3 — Open the File
Launch Power BI Desktop → Click **File → Open** → Select the `.pbix` file.

### Step 4 — Refresh Data (if needed)
If the data source path changes, go to **Home → Refresh** to reload the dataset.

### Step 5 — Explore the Dashboard
- Use the **slicers** on the left or top to filter by date, category, or region
- **Click on any chart** to cross-filter all other visuals
- **Right-click** on a data point to drill down for more detail

---

## 🎯 Use Cases

This dashboard is suitable for:

- 🏪 **Retail businesses** monitoring daily/monthly performance
- 📈 **Sales managers** tracking team and product performance
- 🧑‍💼 **Executives** needing a high-level business overview
- 🎓 **Students & learners** building a Power BI portfolio project
- 💼 **Data analysts** showcasing business intelligence skills

---

## 🚀 Future Improvements

Planned enhancements for future versions:

- [ ] Connect to a **live SQL database** for real-time data refresh
- [ ] Add **AI-powered forecasting** using Power BI's built-in analytics
- [ ] Build a dedicated **mobile-optimized** layout
- [ ] Add **advanced customer segmentation** using RFM analysis
- [ ] Include **budget vs actual** comparison visuals
- [ ] Publish to **Power BI Service** for online sharing

---

## 📚 Key Learnings

Through this project, the following skills were developed and demonstrated:

**Power BI Skills**
- Dashboard design and layout best practices
- Building relationships in the data model
- Creating interactive reports with slicers and drill-downs

**DAX Skills**
- Writing measures for KPIs
- Using `SUM`, `COUNT`, `AVERAGE`, `DIVIDE` functions
- Creating time intelligence calculations

**Data Analytics Skills**
- Cleaning and transforming messy raw data
- Identifying trends and patterns from large datasets
- Translating data into business insights

---

## 👤 Author

**Adnan**
Aspiring Data Analyst

**Skills:** Power BI · SQL · Excel · DAX · Data Cleaning · Data Visualization · Exploratory Data Analysis

---

*This project was built for learning, skill development, and portfolio purposes.*
