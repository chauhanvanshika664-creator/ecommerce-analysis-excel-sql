# ecommerce-analysis-excel-sql
📊 E-commerce SQL Analysis Project (Business Analyst Perspective)

🚀 Project Overview

This project focuses on analyzing an e-commerce dataset using SQL to extract meaningful business insights.

The goal is to simulate how a Business Analyst works with structured data to:

* Understand customer behavior
* Analyze product performance
* Generate insights for business decision-making

⸻

🎯 Objectives

* Analyze customer purchasing patterns
* Segment customers based on spending and behavior
* Evaluate product performance
* Identify revenue trends and opportunities

⸻

🗂️ Dataset Structure

The project is built using three core tables:

1. Customers

* customer_id (Primary Key)
* customer_name

2. Products

* product_id (Primary Key)
* product_name
* price
* product_category

3. Transactions

* transaction_id (Primary Key)
* customer_id (Foreign Key)
* product_id (Foreign Key)
* transaction_date
* total_amount

⸻

🧹 Data Preparation

* Cleaned and structured raw data
* Ensured correct data types
* Handled missing values
* Verified relationships between tables

⸻

🧠 Key Concepts Used

SQL Fundamentals

* SELECT, WHERE, ORDER BY
* GROUP BY, HAVING

Joins

* INNER JOIN
* LEFT JOIN

Aggregation

* SUM(), COUNT(), AVG()

Advanced SQL

* CASE WHEN (Segmentation & Classification)
* Subqueries
* UNION / UNION ALL
* CTE (Common Table Expressions)

Query Optimization

* Avoided SELECT *
* Filtered data early
* Used efficient joins
* Reduced unnecessary computations

⸻

🔍 Analysis Performed

1. Customer Segmentation

* Classified customers into:
    * High Value
    * Medium Value
    * Low Value
* Identified frequent vs occasional buyers

⸻

2. Product Analysis

* Identified most purchased products
* Analyzed revenue contribution by product/category

⸻

3. Product Performance Analysis

* Classified products into:
    * Top Performers
    * Low Performers
    * Dead Products (no sales)
* Used CASE WHEN with aggregation to evaluate performance

⸻

4. Revenue Analysis

* Total revenue calculation
* Revenue by category
* Revenue by customer segment

⸻

5. Behavioral Insights

* One-time vs repeat customers
* Customer purchase patterns
* Order value distribution

⸻

⚡ Sample SQL Snippet

Product Performance Classification
select product_category, sum(`total amount`),
case 
when sum(`total amount`) > 1000 then 'high value'
when sum(`total amount`) between 450 and 1000 then 'medium value'
else 'low value'
end as product_segmentation 
from transaction
group by product_category;

📈 Key Insights

* A small group of customers contributes significantly to overall revenue
* Several products fall into the low-performing or dead category
* High-value customers tend to purchase more frequently
* Revenue is concentrated in specific product categories

⸻

💡 Business Recommendations

* Focus marketing efforts on high-value customers
* Improve retention strategies for one-time buyers
* Optimize product catalog by removing or improving low-performing products
* Invest more in high-performing categories

* ⸻

🛠️ Tools Used

* SQL (MySQL)
* Excel (for validation and exploration)

  
## 📄 Project Report
For detailed analysis and business insights, check the full report here:

[View Report](./REPORT.md)
