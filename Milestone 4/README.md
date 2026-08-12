# Supply Chain Visibility & Optimization
## Milestone 4

## 1. Overview

Milestone 4 focuses on developing a Warehouse Efficiency Dashboard
and an Executive Dashboard using Power BI.

## 2. Warehouse Efficiency Dashboard

The Warehouse Efficiency Dashboard monitors warehouse utilization,
throughput, productivity, inventory efficiency, and warehouse
performance across warehouse, region, and product category.

## 3. Warehouse Utilization Methodology

Warehouse utilization is calculated using the average warehouse
utilization percentage available in the warehouse dimension.

Warehouse Utilization % =
AVERAGE(utilization_%)

The utilization KPI is compared against the warehouse utilization
target of 80%.

## 4. Throughput KPI

Warehouse throughput represents the total quantity processed through
the warehouse during the selected reporting period.

Warehouse Throughput =
SUM(Order Item Quantity)

## 5. Productivity KPI

Warehouse productivity measures the average number of orders handled
per warehouse.

Warehouse Productivity =
Total Orders / Number of Warehouses

## 6. Inventory Turnover

Inventory turnover measures how efficiently inventory is converted
through sales/order activity.

## 7. Executive Dashboard

The Executive Dashboard consolidates key supply chain KPIs including:

- Total Sales
- Total Orders
- Total Profit
- Fillment Rate
- On-Time Delivery
- Warehouse Utilization
- Inventory Turnover
- Supplier Reliability

## 8. Executive Dashboard Design Methodology

The dashboard uses KPI cards, trend charts, regional analysis,
warehouse performance visuals, supplier analysis, inventory analysis,
and interactive slicers.

## 9. Forecasting Implementation

Power BI's Analytics pane forecast functionality is applied to the
sales trend line chart using the order date and total sales measure.

A six-month forecast with a 95% confidence interval is used.

## 10. Drill-Through

Warehouse drill-through functionality allows users to select a
warehouse and navigate to a detailed warehouse performance page.

## 11. Dashboard Optimization

The report was optimized by:

- Removing unnecessary fields
- Reusing DAX measures
- Using a dedicated date table
- Reducing unnecessary visuals
- Optimizing visual interactions
- Checking visual performance using Performance Analyzer
- Maintaining a star-schema data model

## 12. Key Insights

- Warehouse utilization is monitored against the 80% target.
- Warehouse throughput identifies high-volume operational locations.
- Productivity analysis highlights differences between warehouses.
- Supplier reliability supports supplier performance evaluation.
- Inventory turnover identifies inventory efficiency opportunities.
- Sales forecasting supports future planning.
- Regional performance helps identify high-value markets.

## 13. Business Recommendations

- Improve utilization of underperforming warehouse locations.
- Investigate warehouses operating significantly below the target.
- Review high-throughput warehouses for capacity constraints.
- Use supplier reliability metrics for supplier evaluation.
- Monitor slow-moving inventory and improve stock allocation.
- Use sales forecasts to support inventory and warehouse planning.
- Continuously monitor delivery performance.

## 14. Files

Milestone4_PowerBI.pbix

screenshots/Warehouse_Efficiency.png

screenshots/Executive_Dashboard.png
