# Carrefour Retail Performance Dashboard

An end-to-end Power BI dashboard analyzing sales, profitability, customer behavior, and product performance for Carrefour retail stores across Egypt (Cairo, Giza, Alexandria) between 2022 and 2024.

## Overview

This project transforms raw transactional retail data into a 4-page interactive Power BI dashboard that helps stakeholders answer key business questions: which branches perform best, who the customers are, which products drive revenue, and how sales trend over time and by channel.

## Business Questions Answered

- Which store regions, cities, and branches generate the highest net sales and profit?
- How do sales and returns differ by return status across branches?
- What's the customer profile driving revenue — by age group and gender?
- Which order channel (App, Store, Website) do customers use most, and how does that vary by age group?
- What's the completion vs. cancellation vs. return rate of transactions?
- Which product brands and products are the top sellers and most profitable?
- How do sales trend month over month, and what are the peak transaction times?

## Dashboard Pages

### 1. Sales Dashboard
Overview of gross sales, net sales, profit, and quantity sold, broken down by store city, store name, monthly trend, and peak transaction time (morning/afternoon/evening/night).

### 2. Branches Performance
Compares the three store regions (North Coast, Greater Cairo, Delta) and their cities/branches on net sales, returns, and profit, with year and demographic (age group, gender) filters.

### 3. Customer Insights
Analyzes customer behavior: sales by age group and gender, order channel usage by age group, and transaction status breakdown (completed / cancelled / returned) with a return rate KPI.

### 4. Product Dashboard
Breaks down sales, profit, and quantity by brand (HP, Samsung, Fresh, Apple, LG) and by individual product, filterable by year and city.

## Tools Used

- **Power BI Desktop** — data modeling, DAX measures, and dashboard design
- **Power Query** — data cleaning and transformation
- **Excel** — source dataset

## Data Model

The dataset is structured as a star schema with one fact table and several dimension tables:

| Table | Description |
|---|---|
| `Data` (Fact) | Transaction-level records: order/ship dates, customer, segment, location, product, sales, quantity, discount, and profit |
| `Customer` | Customer ID and name |
| `Location` | Store region, city, and state per location ID |
| `Product` | Category, sub-category, and product name per product ID |
| `Segment` | Customer segment lookup |
| `ShipMode` | Shipping method lookup |

## Key Insights

- Greater Cairo and North Coast are the top-performing regions by net sales, with Delta slightly behind.
- Adult customers (age group) generate the highest gross and net sales, followed by Young and Senior groups.
- Store purchases outperform App and Website channels for the Adult segment, while channel usage is more balanced for Young and Senior customers.
- Return rate sits above 50% on several pages, which is worth flagging as a data quality or business concern to investigate further.
- HP and Samsung lead as the top-performing brands by both sales and profit.

## Files in this Repository

```
Carrefour-Retail-Performance-Dashboard/
├── Carrefour.pbix          # Power BI project file
├── Carrefour_Dataset.xlsx  # Source dataset
├── screenshots/            # Dashboard page exports
│   ├── Sales.png
│   ├── Branches.png
│   ├── Customers.png
│   └── Products.png
└── README.md
```

## Screenshots

### Sales Dashboard
![Sales Dashboard](screenshots/Sales.png)

### Branches Performance
![Branches Performance](screenshots/Branches.png)

### Customer Insights
![Customer Insights](screenshots/Customers.png)

### Product Dashboard
![Product Dashboard](screenshots/Products.png)

## How to Explore

1. Download `Carrefour.pbix` and open it in [Power BI Desktop](https://www.microsoft.com/en-us/power-platform/products/power-bi/desktop) (free).
2. Use the year, gender, age group, and channel slicers on each page to filter the data interactively.
3. Navigate between pages using the back arrow / navigation buttons on each screen.

---
*Built as part of my Data Analysis & Business Intelligence learning journey.*
