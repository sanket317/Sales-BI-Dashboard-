
# Power BI Sales Dashboard Project 📊

Welcome to the Power BI Sales Dashboard repository! This project focuses on analyzing sales, profit, orders, profit margin, and other key performance indicators (KPIs) using Power BI. The goal is to provide actionable insights into sales trends, profitability, and customer performance, enabling data-driven decision-making.

## Table of Contents 📚
- [Overview](#overview)
- [Objectives](#objectives)
- [Data Sources](#data-sources)
- [Steps](#steps)
- [Technologies Used](#technologies-used)
- [DAX Measures](#dax-measures)
- [Visualizations](#visualizations)
- [Conclusion](#conclusion)


## Overview 🌟
This project involves:

- **Data Cleaning and Transformation**: Using Power Query to clean and prepare the data for analysis.
- **Data Modeling**: Creating relationships between tables and building a robust data model.
- **DAX Calculations**: Implementing complex calculations using Data Analysis Expressions (DAX).
- **Visualizations**: Designing interactive and insightful dashboards to analyze sales, profit, orders, and more.

The final dashboard provides a comprehensive view of sales performance, profitability, and trends over time.

## Objectives 🎯
The objectives of this project are:

1. **Calculate Total Sales**: Display the total sales value for the selected period.
2. **Calculate Profit**: Visualize the total profit achieved based on sales data.
3. **Analyze Orders**: Analyze the number of orders placed during the selected period.
4. **Calculate Profit Margin**: Calculate and visualize the profit margin percentage.
5. **Compare Sales by Product with Previous Year**: Highlight growth or decline in sales for each product.
6. **Compare Sales by Months with Previous Year**: Identify regions with significant changes in sales.
7. **Display Top 5 Cities**: Showcase the top 5 cities based on sales.
8. **Compare Profit by Channel with Previous Year**: Analyze profitability by sales channel.
9. **Analyze Sales by Customer**: Compare individual customer performance with the previous year.
10. **Create Slicers**: Enable dynamic filtering by date, city, product, and channel.

## Data Sources 📂
The dataset used in this project includes:

- **Sales Data**: Contains information about sales, profit, orders, and other relevant metrics.
- **Date Table**: A custom date table created for time intelligence calculations.

## Steps 🛠️
1. **Gather Data**
   - Collect and validate data from various sources such as databases, spreadsheets, or web services.

2. **Power Query – Data Extract, Transform & Load**
   - Clean and transform data using Power Query (remove duplicates, handle missing values, merge datasets, create calculated columns).

3. **Create a Date Table**
   - Build a custom date table to enable time intelligence calculations in DAX.
   - Turn off "Auto Date/Time" in Power BI settings to improve report performance.

4. **Create Data Model in Power BI Desktop**
   - Design a data model representing relationships between tables.

5. **Develop Reports in Power BI Desktop**
   - Create reports and dashboards using charts, tables, and maps.
   - Apply filters, slicers, and drill-through functionalities.

6. **Implement DAX Calculations**
   - Use DAX to create calculated columns, measures, and tables for advanced computations.

7. **Create Visualizations**
   - **Sales by Product**: Compared with the previous year.
   - **Sales by Month**: Compared with the previous year.
   - **Top 5 Cities by Sales**.
   - **Profit by Channel**: Compared with the previous year.
   - **Sales by Customer**: Compared with the previous year.
   - **Cards**: Displaying Sales, Profit, Profit Margin, and Products Sold.

## Technologies Used 💻
- **Power BI**: For data modeling, DAX calculations, and visualization.
- **Power Query**: For data cleaning and transformation.
- **DAX (Data Analysis Expressions)**: For advanced calculations and measures.

## DAX Measures 📝
### Total Sales
```DAX
Sales = SUM(Sales_Data[Sales])
```
### Previous Year Total Sales
```DAX
Sales PY = CALCULATE([Sales], SAMEPERIODLASTYEAR(DateTable[Date]))
```
### Difference Between Current Year Sales & Previous Year Sales
```DAX
Sales vs PY = [Sales] - [Sales PY]
```
### Percentage Increase or Decrease in Sales Year on Year (YOY%)
```DAX
Sales vs PY % = DIVIDE([Sales vs PY], [Sales], 0)
```
### Products Sold
```DAX
Products Sold = SUM(Sales_Data[Order Quantity])
```
### Profit
```DAX
Profit = SUM(Sales_Data[Profit])
```
### Profit Last Year
```DAX
Profit LY = CALCULATE([Profit], SAMEPERIODLASTYEAR(DateTable[Date]))
```
### Profit vs Last Year
```DAX
Profit vs LY = [Profit] - [Profit LY]
```
### Profit vs Last Year Percentage
```DAX
Profit vs LY % = DIVIDE([Profit vs LY], [Profit], 0)
```
### Profit Margin
```DAX
Profit Margin = DIVIDE([Profit], [Sales], 0)
```
### Total Cost
```DAX
Total Cost = SUM(Sales_Data[Total Cost])
```

## Visualizations 📊
- **Sales by Product**: Compared with the previous year.
- **Sales by Month**: Compared with the previous year.
- **Top 5 Cities by Sales**.
- **Profit by Channel**: Compared with the previous year.
- **Sales by Customer**: Compared with the previous year.
- **Cards**: Displaying Sales, Profit, Profit Margin, and Products Sold.

## Conclusion 📝
### Key Insights for the Year 2019:
- Sales decreased by more than 10%.
- There is a drop in sales for all the top 7 products.
- 4 customers are leading to a drop in sales.
- The profit margin in the Export channel is higher.


