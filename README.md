**AtliQ** hardware is a company in India which supplies computer hardware and peripheral devices across India only.

**Scenario —**

The sales manager of the company is facing many challenges. He is facing issues in tracking sales in dynamically growing market.He is having issues with the insights of his business.

In order to this he has some of the regional managers in North, south and central India working for the company. So, he calls them and ask about the insights he wants to know. They tell him about the sales in last quarter and the growth in that quarter.

So, in this project we will help a company make its own sales related dashboard using PowerBI.

**How will the company work —**

There is a team of software engineers (falcons) which owns sales management system. The records of this system are stored in MySQL database.

In this same manner our project is going to be executed. We are going to fetch the data from the database from company’s website and then we are going to transform and load the data in the PowerBI to build the dashboard.

**Data Analysis using SQL**

Step 1: Importing Data to MySQL workbench
Step 2: Simple analysis of data by looking into different tables and reflecting garbage values
Step 3: Primary analysis of data base by running different SQL statements

**Data Cleaning and ETL (extract transform load)**

Step 1: We are going to connect MySQL with the PowerBI dektop
Step 2: Loading the data into the PowerBI desktop
Step 3: Transforming data with the help of Power Query

**Building a Dashboard or a Report**

Dashboards/reports are created according to the requirement. What actually the company wants to look for and what is more important for the company is taken into consideration and then after the dashboard is created. There can be n number of variations to create a dashboard. Generally, the dashboard should look understandable and an ease to access.

**Data Analysis Using SQL**:

1. Show all customer records

SELECT * FROM customers;

2. Show total number of customers

SELECT count(*) FROM customers;

3. Show transactions for Chennai market (market code for chennai is Mark001

SELECT * FROM transactions where market_code='Mark001';

4. Show distrinct product codes that were sold in chennai

SELECT distinct product_code FROM transactions where market_code='Mark001';

5. Show transactions where currency is US dollars

SELECT * from transactions where currency="USD"

6. Show transactions in 2020 join by date table

SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;

7. Show total revenue in year 2020,

SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";

8. Show total revenue in year 2020, January Month,

SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");

9. Show total revenue in year 2020 in Chennai

SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.market_code="Mark001";
