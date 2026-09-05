# Project Report: E-Commerce Sales & Profitability Analysis

## Executive Summary

This report summarizes the work behind the **E-Commerce Sales & Profitability Analysis** Power BI project. The goal was to take raw transactional data from an e-commerce business and turn it into a decision-ready dashboard covering sales performance, profitability, customer value, regional performance, and the impact of discounting. The finished report spans 7 pages and is powered by a star-schema data model with 17 custom DAX measures.

Across the ~2,000 transactions analyzed, the business generated approximately **$2.55M in gross sales** and **$1.08M in revenue** (after cost and discount), at an average order value of roughly **$539**. The analysis surfaced clear differences in performance by category, region, and customer segment, summarized below.

## Objective

The project set out to answer four core business questions:

1. Which product categories and regions are the strongest and weakest performers?
2. Who are the most valuable customers, and how much do they contribute to revenue?
3. How does discounting affect profit margin across product categories?
4. How are sales trending over time (month-over-month and year-over-year)?

## Data Overview

The analysis is built on five tables in a star-schema layout:

| Table | Rows | Contents |
|---|---|---|
| `Sales_Fact` | 2,000 | Transaction-level sales: date, quantity, unit price, discount, payment type, revenue |
| `Dim_Customer` | 500 | Customer name, demographics, and loyalty tier |
| `Dim_Product` | 100 | Product name, category, sub-category, brand, cost, stock |
| `Dim_Store` | 20 | Store name, region, city, store type |
| `Dim_Calender` | — | Date table supporting time-intelligence calculations |

Transactions cover **October 2023 – October 2025**, across **5 categories** (Electronics, Clothing, Beauty, Home, Sports), **4 regions** (East, North, South, West), and **3 payment types** (Credit Card, PayPal, COD).

## Methodology

1. **Data modeling** — Related the fact table to each dimension table (Customer, Product, Store) on their respective keys, and connected a date table for time intelligence.
2. **DAX measure development** — Wrote 17 measures covering core KPIs (Total Sales, Revenue, Profit, Profit Margin %, Total Orders, Average Order Value), ranking logic (Customer Rank, Top 10 Customers), and time intelligence (YTD, Month-over-Month Growth, Same-Period-Last-Year comparisons).
3. **Report design** — Built 7 report pages moving from a high-level executive summary (My Dashboard) into focused views: Sales Analysis, Product Analysis, Customer Analysis, Regional Analysis, Discount Analysis, and Time Analysis.
4. **Interactivity** — Added slicers for Year, Region, and Category on the executive dashboard so results can be filtered without touching the underlying model.

## Key Findings

**Category performance:** Sports generated the highest revenue (~$324K), followed by Home (~$227K), Electronics (~$183K), Clothing (~$180K), and Beauty, the lowest performer (~$163K) — despite Electronics having the highest gross sales, its revenue after cost and discount trails Sports and Home.

**Regional performance:** South, North, and East regions perform similarly (roughly $307K–$326K in revenue each), while **West lags noticeably behind** at ~$134K — less than half of any other region — making it the weakest-performing region and a candidate for further investigation.

**Customer value:** The top 5 customers by revenue each contributed between roughly $9K and $11.8K, led by Casey Simpson (~$11.8K). At the segment level, **Platinum-tier customers generated the most total revenue (~$334K)**, ahead of Gold (~$257K), Bronze (~$254K), and Silver (~$232K) — loyalty tier correlates with revenue contribution, though the gap between tiers other than Platinum is fairly narrow.

**Discounting:** Discounts applied across transactions ranged from 0% to 30%, averaging **~14.8%**, with the middle 50% of transactions discounted between 7% and 23%. The Discount Analysis page cross-references discount levels against profit margin by category to flag where heavier discounting is eroding margin.

**Payment methods:** Sales are fairly evenly split across payment types, with PayPal slightly ahead (~$885K) over Credit Card (~$842K) and COD (~$827K) — no single payment method dominates.

## Business Recommendations

- **Investigate the West region's underperformance** — with less than half the revenue of other regions, it's worth checking store count, staffing, local demand, or marketing spend in that region.
- **Protect margin in heavily discounted categories** — use the Discount Analysis page to identify categories where discounting is cutting most into profit, and consider tightening promotional depth there.
- **Grow the Beauty and Clothing categories** — as the lowest revenue contributors, these may benefit from targeted promotions or expanded product assortment.
- **Deepen engagement with Platinum and Gold customers** — since these segments already drive the most revenue, loyalty perks or upsell campaigns aimed at this group have a clear high-value target.

## Tools & Skills Demonstrated

- **Power BI Desktop** and **Power Query** for data modeling and transformation
- **DAX**: aggregation functions (`SUMX`, `DIVIDE`), ranking (`RANKX`), conditional logic (`IF`), and time intelligence (`TOTALYTD`, `SAMEPERIODLASTYEAR`, `PREVIOUSMONTH`)
- Star-schema data modeling and relationship design
- Interactive dashboard design with cross-filtering slicers
- Business analysis: profitability breakdown, customer segmentation, discount-impact analysis, and regional performance comparison

## Conclusion

This project demonstrates an end-to-end Power BI workflow — from a raw star-schema dataset to a fully interactive, multi-page dashboard — while surfacing concrete, actionable business insights: a clear underperforming region, a defined set of high-value customers, and measurable trade-offs between discounting and profit margin. The combination of the `.pbix` file and this report gives a complete picture of both the technical build and the business value delivered.
