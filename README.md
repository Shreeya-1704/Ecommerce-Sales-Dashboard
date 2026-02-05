# E-commerce Sales Dashboard

This project analyzes online sales data to uncover revenue drivers, customer behavior, and product performance.  
Using Power BI for data transformation and visualization, the dashboard highlights order trends, category-wise sales, and customer segments to support business growth strategies.

# Problem Statement
E-commerce businesses need to track sales, profit, and customer trends to optimize marketing, inventory, and operations.  
This project identifies top-selling categories, high-value customers, and seasonal demand patterns to guide strategic decisions.

## Tools & Skills
- Power BI (data cleaning, transformation, and interactive dashboards)

# Workflow
1. Imported raw order and product detail data into Power BI.
2. Transformed data (handled missing values, duplicates, created calculated columns such as profit margin).
3. Built interactive dashboards showing KPIs, monthly trends, category performance, and customer insights.
4. Summarized findings into actionable recommendations.

# Potential Extensions with SQL
Although this project was built entirely in Power BI, SQL could be used in a real-world scenario to query data directly from the database:
```sql
-- Total revenue by category
SELECT Category, SUM(Sales) AS TotalRevenue
FROM Orders
GROUP BY Category;

-- Top 10 customers by sales
SELECT CustomerName, SUM(Sales) AS TotalSales
FROM Orders
GROUP BY CustomerName
ORDER BY TotalSales DESC
LIMIT 10;

-- Monthly sales trend
SELECT MONTH(OrderDate) AS Month, SUM(Sales) AS MonthlySales
FROM Orders
GROUP BY MONTH(OrderDate);
