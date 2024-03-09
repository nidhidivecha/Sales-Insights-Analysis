# Sales-Insights-Analysis

## **Project Explanation**

### **About Project**

* Performed Data Cleaning, Analysing and Visualization on India based hardware company sales insights.

* Developed ETL mappings using SQL to extract the data from unstructured data and transformed it to the staging area to conduct data cleaning and design star schema data model on Power BI.

* Developed a Power BI dashboard to perform analysis, producing quantitative visualizations in Tableau to draw valuable insights based on different parameters affecting the company performance year on year and further provide business solutions.

### **About ATLIQ**

* AtliQ Hardware is Computer Hardware and peripheral Manufacture company.

### **Technologies Used**

* Advance Excel

* MySQL

* Power BI

* Statistics

### **Problem Statement**

Sales director wants to know the performance of the company in various Indian states & accordingly provide some discount.

Q1. Revenue breakdown by cities.

Q2. Revenue breakdown by years & months.

Q3. Top 5 customers by revenue & sales quantity.

Q4. Top 5 Products by revenue.

Q5. Net Profit & Profit Margin by Market.

### **Aim of the Project**

To unlock sales insights that are not visible before for sales team for decision support & automate them to reduced manual time spent in data gathering.

**Stake Holders: Who will be involved?** 

* Sales Director
* I.T. Team
* Customer Service Team
* Data & Analytics Team

**End Result: What do we want to achieve?**

* An automated dashboard providing quick & latest sales insights in order to support data driven decision making.

**Success Criteria: What will be our success criteria?**

* Dashboards uncovering sales order insights with latest data available.
* Sales team able to take better decision & prove 10% cost savings of total spend.
* Sales analysts stop data gathering manually in order to save 20% of their business time & reinvest it in value added activity.


## **Data Analysis Using SQL**

-- Show all customer records

SELECT * FROM customers;

-- Show total number of customers

SELECT COUNT(*) AS total_customers FROM customers;

-- Show transactions for Chennai market (market code for Chennai is Mark001)

SELECT * FROM transactions
WHERE market_code = 'Mark001';

-- Show distinct product codes that were sold in Chennai.

SELECT DISTINCT product_code
FROM transactions
WHERE market_code = 'Mark001';

-- Show transactions where currency is US dollars.

SELECT * FROM transactions
WHERE currency = 'USD';

-- Show transactions in 2020 join by date table.

SELECT transactions.*, date.*
FROM transactions
INNER JOIN date ON transactions.order_date = date.date
WHERE date.year = 2020;

-- Show total revenue in the year 2020.

SELECT SUM(transactions.sales_amount) AS total_revenue_2020
FROM transactions
INNER JOIN date ON transactions.order_date = date.date
WHERE date.year = 2020
AND (transactions.currency = 'INR' OR transactions.currency = 'USD');

-- Show total revenue in the year 2020, January Month.

SELECT SUM(transactions.sales_amount) AS total_revenue_jan_2020
FROM transactions
INNER JOIN date ON transactions.order_date = date.date
WHERE date.year = 2020
AND date.month_name = 'January'
AND (transactions.currency = 'INR' OR transactions.currency = 'USD');

## **Power BI Dashboard : Key insights**

## **Power BI Dashboard : Profit Analysis**

## **Power BI Dashboard : Performance Insights**
