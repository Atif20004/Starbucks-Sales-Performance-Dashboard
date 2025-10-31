# Starbucks Sales Performance Dashboard — Power BI Project
## Project Overview

The Starbucks Sales Performance Dashboard is a comprehensive data analysis project built using Power BI, aimed at understanding and visualizing the overall sales performance, product trends, and store-level insights for Starbucks.
The goal of this project is to convert raw transactional and product data into meaningful and actionable business insights.

This interactive dashboard allows business users, managers, and analysts to explore key sales metrics such as Total Revenue, Total Quantity Sold, Average Sales per Order, and Average Price per Product, along with detailed breakdowns by product category, store location, size, and time period.

Through this project, I have applied my knowledge of data cleaning, data modeling, DAX calculations, relationship creation, and visualization design to build an analytics solution that mirrors real-world retail business reporting.

## Project Objectives
The primary objectives of this project were:
1.	To analyze and visualize sales performance across multiple dimensions such as product type, category, and store location.
2.	To identify top-performing products contributing to the majority of sales revenue.
3.	To examine sales trends over months, quarters, and the entire year to understand seasonal variations.
4.	To highlight average price distribution and the impact of product size on total sales.
5.	To develop an interactive and user-friendly Power BI dashboard that allows dynamic filtering and data exploration.

## Dataset Used
- <a href="https://github.com/Atif20004/Starbucks-Sales-Performance-Dashboard/blob/main/Orders_Table_.csv"> Orders_Table_ </a>
- <a href="https://github.com/Atif20004/Starbucks-Sales-Performance-Dashboard/blob/main/Products_Table_.csv"> Products_Table_ </a>


## Business Questions for Analysis

### Advanced Analytical Questions

These questions are addressed using Power BI measures, DAX formulas, and visual analytics created from the available dataset.

1. How do product returns or order cancellations impact overall profitability?
2. Which time slots or days of the week generate the highest sales?
3. Are there differences in sales performance during weekdays vs. weekends?
4. Which products show the highest growth rate in both sales quantity and revenue value?
5. How do price changes, discounts, or markdowns affect overall demand by product category?
6. How does store location type (e.g., mall, airport, streetfront) influence the average sale value?
7. Are there regional or city-specific preferences in product selection?
8. What is the customer purchasing frequency — repeat customers vs. new customers?
9. What’s the trend in sales per employee or footfall per store location?
10. Are there cross-selling opportunities between product categories (e.g., Coffee & Bakery)?

###  Future Insights & Strategic Analysis

These questions are designed for advanced exploration and business forecasting — useful for extending the dashboard with predictive insights in the future.

1. How effective are seasonal promotions in boosting sales of specific product categories?
2. How does the introduction of new products or SKUs impact the sales of existing items?
3. What is the estimated stock-out or lost sales percentage for top-performing SKUs?
4. How does product bundling or combo offers influence overall revenue?
5. What are the potential opportunities to increase average transaction value based on customer purchase behavior?

 ##  Project Process
### *1. Data Understanding*
•	Explored both ORDER and PRODUCT tables to decide which KPIs are relevant and how they can be derived.

•	Identified join keys, categorical and numeric fields, and columns that needed standardization (locations, product sizes, categories).

### *2. Data Cleaning & Transformation (Power Query)*

•	Removed duplicates and empty/invalid rows for order transactions.

•	Standardized text fields (case, spelling, naming).

•	Joined the ORDER and PRODUCT tables on product_id for analysis.

•	Made sure all dates were in proper Date type; extracted month/year for time-based slicing.

### *3. Calculated Fields & DAX Metrics*
•	Total_Sale: SUMX('ORDER','ORDER'[transaction_qty]*RELATED('PRODUCT'[unit_price]))

  Dashboard Value: *₹59M* 
  
•	Total_Quantity_Sold: SUM('ORDER'[transaction_qty])

 Dashboard Value: *214K*
 
•	Avg_Sales_per_Order: DIVIDE([Total_Qty_Sold], DISTINCTCOUNT('ORDER'[transaction_id]))

 Dashboard Value: *1.44* 
 
•	Avg_Price_per_Product: AVERAGE(product[unit_price])

Dashboard Value: *₹560* 

### *4. Dashboard Design & Iteration*
•	Selected visuals answering the KPIs above: Bar chart, line chart, pie chart, KPI card, interactive table, donut chart.

•	Iterated on interactive layout for user clarity and storytelling: summary cards, sales trends, location/size charts, top products detail table.

•	Slicer panel for month, location, and size to allow users to easily focus their analysis.

## Dashboard Interaction




