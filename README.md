# Retail Sales Performance Dashboard — Excel

An end-to-end Excel analytics project covering data cleaning, calculated fields, PivotTables, and an interactive dashboard, built on a 4-table relational retail dataset (Orders, Products, Customers, Employees — 400+ transactions).

## Overview
This project simulates a real business scenario: raw, messy transactional data that needs to be cleaned, joined, and turned into an executive-ready dashboard.

## Data Cleaning
- Standardized inconsistent customer name formatting (extra spaces, mixed case) using `TRIM` + `PROPER`
- Identified and resolved 4 duplicate OrderIDs — distinguished true duplicates from ID collisions (same ID reused for different orders) and reassigned new unique IDs
- Investigated blank Quantity values instead of imputing an average; flagged them as "Cancelled Order" in a dedicated data-quality column, preserving reporting transparency

## Calculated Fields
- Joined Product, Customer, and Employee details into Orders using `VLOOKUP`
- Built `Total Amount` (Quantity × Selling Price) and `Revenue` (Total Amount × (1 − Discount))

## Analysis (PivotTables & Charts)
- **Revenue & Orders by Region** — dual-axis combo chart
- **Revenue by Category** — bar chart (chosen over pie chart due to 8 categories being hard to compare as slices)
- **Revenue & Orders by Employee** — dual-axis combo chart
- **Year-over-Year Monthly Trend** — line chart comparing Jan–Jun 2024 vs Jan–Jun 2025

## Key Insights
- Home & Kitchen had the highest average revenue per order (₹15,100), despite fewer total orders than Electronics — a smaller but higher-value customer segment
- Rohit Sinha had the highest average revenue per sale among employees, despite Priya Nair leading in total revenue and order count
- Revenue for Jan–Jun 2025 was ~4.8% lower than the same period in 2024 (a precise same-period comparison, not a full-year vs. half-year estimate)

## Dashboard
Interactive one-page dashboard with KPI cards (Total Revenue, Total Orders), slicers (Region, Category, Employee), and 4 linked charts.

*(Add your dashboard screenshot here after uploading — drag the image into the README editor or use `![Dashboard](screenshot.png)`)*

## Tools Used
Microsoft Excel — VLOOKUP, PivotTables, PivotCharts, TRIM/PROPER, conditional flagging, slicers
