# Superstore-sales--dashboard-powerbi
Superstore Sales Performance Dashboard
Overview
Interactive Power BI dashboard analyzing 4 years of US retail sales data (9,994 transactions, 2014–2017) to identify revenue trends, regional performance gaps, and profitability drivers across product categories and sub-categories.
Built as part of a self-directed data analytics portfolio to demonstrate end-to-end skills in data cleaning, DAX measure creation, and business storytelling through visualization.

# Tools & Technologies

Power BI Desktop — Dashboard design, DAX measures, conditional formatting
Power Query — Data type correction, column cleanup, date format standardization
DAX — Custom measures for Total Sales, Profit Margin %, Avg Order Value
Data Source — Sample Superstore Dataset (Kaggle)

#Key Business Findings

- West region leads in revenue at the highest sales contribution among all 4 regions, but South region consistently underperforms
- Technology is the most profitable category — highest profit margin across Furniture, Office Supplies, and Technology
- Furniture category is a margin problem — decent sales volume but near-zero profit, dragged down by deep discounting
- 3 loss-making sub-categories identified: Tables, Bookcases, and Supplies generate negative profit despite positive sales — discount rates are destroying margins
- Seasonal spike visible every year — October to December consistently peaks, indicating inventory and staffing planning opportunity
- Sean Miller is the top customer by total revenue
- Top 10 customers account for a disproportionate share of total revenue — concentration risk worth monitoring


# Dashboard Metrics
MetricValueTotal Sales = $2.30M
Total Profit = $286.40K
Profit Margin % = 12.5%
Total Orders = 5,009
Date Range = January 2014 – December 2017
Total Records = 9,994 transactions

# Dashboard Features

-4 KPI Cards — Total Sales, Total Profit, Profit Margin %, Total Orders
-Monthly Sales Trend Line Chart — 48-month view showing growth trajectory and seasonal patterns
-Sales by Region Bar Chart — Ranked by revenue with data labels
-Profit by Category Column Chart — Technology vs Office Supplies vs Furniture
-Top 10 Customers Bar Chart — Filtered using Top N filter by Total Sales
-Sub-Category Profit Chart — Conditional formatting applied: red bars = loss-making, green = profitable
-Interactive Slicers — Filter entire dashboard by Region and Customer Segment (Consumer / Corporate / Home Office)


# Technical Highlights
Power Query transformations:

Fixed date format errors caused by regional locale conflict (US MM/DD/YYYY vs system DD/MM/YYYY) using "Change Type Using Locale"
Removed Postal Code column to prevent incorrect numeric aggregation
Standardized data types across all columns (Date, Decimal, Whole Number)

# DAX measures created:
Total Sales = SUM(Orders[Sales])
Total Profit = SUM(Orders[Profit])
Profit Margin % = DIVIDE([Total Profit], [Total Sales], 0)
Total Orders = DISTINCTCOUNT(Orders[Order ID])
Avg Order Value = DIVIDE([Total Sales], [Total Orders], 0)
Conditional formatting logic:

Sub-category bars turn red when Total Profit < 0 (loss-making)
Immediately surfaces Tables, Bookcases, and Supplies as problem areas


# Files in This Repository
Superstore_Sales_Dashboard_DivyanshChaudhary.pbix - Power BI source file
Superstore_Sales_Dashboard_DivyanshChaudhary.pdf - Exported PDF of the dashboard
superstoresales-dashboard-screenshot.png - Dashboard preview image
README.md - This file

# How to Open

1) Download and install Power BI Desktop (free)
2) Clone or download this repository
3) Open Superstore_Sales_Dashboard_DivyanshChaudhary.pbix in Power BI Desktop
4) All data is embedded — no external connections required


# About
Built by Divyansh Chaudhary
B.Com (Hons) — Shyam Lal College, University of Delhi
Targeting entry-level roles in Data Analytics, Business Analytics, MIS, Analytics, Operations, and Research
www.linkedin.com/in/divyansh-chaudhary-b67a13254 - LinkedIn 
GitHub
