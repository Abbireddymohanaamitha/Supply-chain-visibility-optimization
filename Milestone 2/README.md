# Supply Chain Visibility & Optimization – Milestone 2

## Project Overview

This project focuses on analyzing supply chain operations using Power BI. The dashboard provides insights into inventory management, warehouse utilization, supplier performance, sales trends, and delivery performance to support data-driven business decisions.

---

## Tools & Technologies

- Power BI Desktop
- Power Query Editor
- DAX (Data Analysis Expressions)
- PostgreSQL
- Microsoft Excel
- GitHub

---

## Data Modeling

A Star Schema data model was implemented consisting of one Fact Table and multiple Dimension Tables:

- Fact_table
- Dim_Customer
- Dim_Product
- Dim_Category
- Dim_Department
- Dim_Shipping
- Dim_Location
- Dim_Date
- Dim_Supplier
- Dim_Warehouse
- Dim_Inventory

---

# Inventory Turnover Calculation Approach

Inventory Turnover Ratio measures how efficiently inventory is sold during the reporting period.

### DAX Formula

```DAX
Inventory Turnover Ratio =
DIVIDE(
    [Total Sales],
    [Avg Inventory Value],
    0
)
```

### Interpretation

- Higher ratio indicates inventory is moving quickly.
- Lower ratio indicates inventory is staying longer in warehouses.
- Helps optimize purchasing and inventory planning.

---

# Slow-Moving and Fast-Moving Inventory Identification Logic

Inventory movement is identified by comparing Stock Quantity, Sales, and Reorder Level.

### Fast-Moving Inventory

Products with:

- High sales volume
- High inventory turnover
- Frequent restocking
- Low warehouse storage duration

These products require continuous inventory replenishment.

### Slow-Moving Inventory

Products with:

- Low sales
- High stock quantity
- Low inventory turnover
- Long storage duration

These products increase storage costs and should be monitored carefully.

---

# Delivery Performance Analysis Methodology

Delivery performance is analyzed using delivery-related KPIs and DAX measures.

### KPIs Used

- Total Orders
- On-Time Delivery Rate
- Late Delivery Percentage
- Advance Shipping Percentage
- Average Supplier Lead Time
- Average Shipping Days

### DAX Example

```DAX
On-Time Delivery Rate =
DIVIDE(
    CALCULATE(
        COUNTROWS(Fact_table),
        Fact_table[Late_delivery_risk] = 0
    ),
    COUNTROWS(Fact_table)
)
```

### Analysis Performed

- Region-wise delivery performance
- Delivery status distribution
- Delivery trend over time
- Supplier lead time comparison
- Shipping performance analysis

---

# Dashboard Features

## Delivery Performance Dashboard

KPIs

- Total Sales
- Total Profit
- Total Orders
- On-Time Delivery Rate
- Average Supplier Lead Time

Visualizations

- Sales by Region
- Orders by Category
- Delivery Status Distribution
- Sales Trend
- Supplier Performance Table
- Delivery Risk Gauge

---

## Inventory Analytics Dashboard

KPIs

- Inventory Turnover Ratio
- Total Stock Quantity
- Total Reorder Level
- Total Inventory Value

Visualizations

- Inventory Value by Warehouse
- Inventory Distribution by Warehouse
- Sales by Category
- Stock Quantity vs Reorder Level
- Inventory Trend by Region

---

# Key Insights

- Warehouses have varying inventory values, indicating different storage capacities and utilization.
- High-selling product categories require frequent inventory replenishment.
- Products with low sales and high stock levels represent slow-moving inventory.
- Inventory Turnover Ratio helps evaluate inventory efficiency.
- Delivery performance varies across regions and can be monitored using on-time and late delivery metrics.
- Supplier lead time directly impacts delivery performance and inventory availability.

---

# Business Recommendations

- Maintain adequate stock for high-demand products to prevent stock shortages.
- Reduce excess inventory for slow-moving products to minimize holding costs.
- Monitor reorder levels regularly for timely replenishment.
- Improve supplier selection based on lead time and reliability.
- Optimize warehouse inventory distribution for better space utilization.
- Continuously monitor delivery KPIs to improve customer satisfaction.
- Use dashboard insights for demand forecasting and inventory planning.

---

# Repository Structure

```
Supply_Chain_Visibility_Optimization/
│
└── Milestone 2/
    ├── Milestone2_PowerBI.pbix
    ├── README.md
    └── screenshots/
        ├── Delivery_Performance.png
        └── Inventory_Analytics.png
```

---

# Conclusion

This project demonstrates the use of Power BI for supply chain analytics by integrating data transformation, data modeling, DAX calculations, and interactive dashboards. The solution provides actionable insights into inventory management, warehouse operations, supplier performance, and delivery efficiency, enabling organizations to make informed business decisions.
