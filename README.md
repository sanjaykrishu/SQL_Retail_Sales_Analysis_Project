Retail Sales Data Analysis – SQL Project Report

1. Project Overview
The aim of this project is to analyze retail sales data stored in a SQL database, perform data cleaning, and generate insights through various SQL queries. The dataset contains transaction-level sales records including details like date, time, customer demographics, product category, and sales amount.

2. Database & Table Structure
Table Name: retail_sales

Columns:

transactions_id (INT, PRIMARY KEY) – Unique transaction identifier

sale_date (DATE) – Date of transaction

sale_time (TIME) – Time of transaction

customer_id (INT) – Customer identifier

gender (VARCHAR(15)) – Gender of the customer

age (INT) – Age of the customer

category (VARCHAR(15)) – Product category

quantity (INT) – Quantity sold

price_per_unit (FLOAT) – Price per unit

cogs (FLOAT) – Cost of goods sold

total_sale (FLOAT) – Total sale amount

3. Data Preparation & Cleaning
Step 1: Dropped existing retail_sales table if it exists.

Step 2: Created the table with defined schema.

Step 3: Checked for NULL values across all columns.

Step 4: Deleted rows with NULL values to ensure data quality.

4. Data Exploration
Total number of sales transactions – Count of all records.

Total unique customers – Count of distinct customer_id.

Number of categories – Count of distinct product categories.

5. Key Business Queries & Insights
Q1: Sales made on 2022-11-05 – Retrieve all columns for that date.
Q2: Clothing category sales (≥ 4 quantity) in Nov 2022 – Filtered transactions.
Q3: Total sales per category – Summarized total_sale by category.
Q4: Average age of customers for Beauty category – Calculated mean age.
Q5: Transactions with sales > 1000 – High-value transactions.
Q6: Number of transactions by gender per category – Grouped count.
Q7: Best-selling month per year – Used RANK() to identify top months by average sales.
Q8: Top customers by sales – Ranked by SUM(total_sale) (note: LIMIT in query shows only top 1, should be LIMIT 5 for top 5).
Q9: Unique customers per category – Count of distinct buyers by category.
Q10: Orders by shift (Morning < 12, Afternoon 12–17, Evening > 17) – Classified using CASE logic.

6. Analytical Observations
Cleaning process ensured no NULL values in the dataset.

Categories have varied customer bases; top categories can be identified using Q3 & Q9 results.

Seasonal patterns can be tracked using Q7 for marketing strategy.

High-value customers identified in Q8 can be targeted for loyalty programs.

Sales distribution by shift (Q10) helps in resource allocation (e.g., staffing).

