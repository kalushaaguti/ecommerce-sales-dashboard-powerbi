🚀Project Summary

This project is an interactive Power BI Business Intelligence dashboard developed to analyze sales performance and profitability for an e-commerce dataset.
The dashboard provides executives and business teams with a clear overview of:
Revenue generation
Profitability trends
Product performance
Shipping efficiency
Geographic sales distribution

🎯 Business Questions Answered

The report was designed to address key sales and profitability metrics, including:
Total Sales by Product Category
Profit Ratio for Each Country
Sales vs Profit Relationship
Total Sales by Shipping Carrier
Total Sales by Ship Mode
Total Sales by Subcategory
Overall KPIs: Total Sales, Total Profit, Profit Ratio
Full report filtering by State

📌 Dashboard Features
✅ Key Performance Indicators (KPIs)
Total Sales
Total Profit
Profit Ratio

📦 Sales Breakdown Analysis

Category-level sales distribution
Subcategory performance ranking
Carrier contribution to revenue
Ship mode sales comparison

🌍 Geographic Profitability Insights

Profit ratio analysis by country
State-level filtering for regional drilldowns

📈 Sales vs Profit Analysis

A scatter plot visual highlights the relationship between:
High revenue products
Low vs high profitability segments

🗂️ Data Model Structure

The report uses a star schema approach:
| Table Type         | Table Name |
| ------------------ | ---------- |
| Fact Table         | 2023_Sales |
| Dimension          | Products   |
| Dimension          | Shipping   |
| Dimension          | Store      |
| Optional Dimension | Customer   |

Relationships were built using unique IDs:

ProductID
ShippingID
StoreID
CustomerID

🧮 DAX Measures Implemented
Total Sales

Total Sales =
SUMX(
    '2023_Sales',
    '2023_Sales'[Quantity] *
    RELATED(Products[Unit Price (MRP)]) *
    (1 - '2023_Sales'[Discount])
)

Total Profit

Total Profit = SUM('2023_Sales'[Profit])

Profit Ratio

Profit Ratio = DIVIDE([Total Profit], [Total Sales])

🛠️ Tools & Skills Demonstrated

Power BI Desktop
Power Query (data cleaning & transformation)
Data Modeling & Relationships
DAX Calculations
Interactive Dashboard Design
Business Intelligence Reporting

Repository Contents
📁 Ecommerce-Sales-Dashboard
│── Ecommerce_Sales_Dashboard.pbix
│── Dashboard_Report.pdf
│── README.md
└── assets/
    └── dashboard.png
