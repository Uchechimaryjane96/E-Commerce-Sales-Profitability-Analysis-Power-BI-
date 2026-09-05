# E-Commerce Sales Analysis Dashboard (Power BI)

## Project Overview
End-to-end Power BI project analyzing e-commerce sales performance — covering revenue, profit, customer behavior, regional performance, discounting, and time trends. Built on a star-schema data model connecting a central sales fact table to product, store, customer, and calendar dimensions.

## Project Workflow
1. **Data Modeling** — Built a star schema linking `Sales_Fact` to `Dim_Product`, `Dim_Store`, `Dim_Customer`, and `Dim_Calendar`.
2. **DAX Measures** — Created calculated measures for Total Sales, Profit, Profit Margin %, Total Orders, Average Order Value, Discount impact, and Customer Ranking.
3. **Interactive Report Design** — Built 7 report pages: an executive summary and six focused analysis views.
4. **Slicers & Filters** — Added Year/Month, Region, and Category slicers for dynamic, cross-page filtering.
5. **Insights & Recommendations** — Surfaced top customers, loss-making products, and regional performance gaps.

## Tools Used
- Power BI Desktop (Data Modeling, DAX, Visualization)
- DAX (Data Analysis Expressions) for measures
- Power Query (data cleaning & transformation)

## Report Pages
1. **My Dashboard** — Executive summary with KPI cards (Profit, Total Sales, Profit Margin %, Total Orders) plus category, region, and brand breakdowns
2. **Sales Analysis** — Revenue and profit trends by category and by year/month
3. **Product Analysis** — Category- and brand-level profit, profit margin, and loss-making product detection
4. **Customer Analysis** — Average order value and Top 10 customers by revenue
5. **Regional Analysis** — Sales by region, lowest-profit region, regional breakdown table
6. **Discount Analysis** — Discount impact on profit margin and sales by category
7. **Time Analysis** — Year/month sales trend table

## Key Measures (DAX)
- Total Sales
- Profit
- Profit Margin %
- Total Orders
- Average Order Value
- Top 10 Customers
- Customer Rank / Customer Rank Revenue
- Lowest Profit Region
- Loss Product

## Data Model
Star schema:
- `Sales_Fact` (fact table)
- `Dim_Product`
- `Dim_Store`
- `Dim_Customer`
- `Dim_Calendar`

## Key Insights
> Replace these with your actual headline numbers before publishing:
- Total Sales: $__
- Total Profit: $__
- Profit Margin: __%
- Top Region: __
- Top Customer: __
- Highest-Discount Category: __

## Dashboard
![Dashboard](dashboard.png)
*(Export a screenshot of your "My Dashboard" page as `dashboard.png` and place it in the repo root so it renders here.)*

## Skills Demonstrated
- Data Modeling (Star Schema)
- DAX (Measures & Calculated Columns)
- Power BI Report Design
- Sales / Customer / Regional / Discount Analytics
- KPI Design & Data Storytelling

## Files
- `MY_ECOMMERCE_PROJECT_PBI.pbix`
- `dashboard.png` — dashboard screenshot (add your own)
- `README.md`
