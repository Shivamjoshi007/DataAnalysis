Data Analysis Project - Sales Insights
======
- This Repositary consists two Tableau dashboards, representing the sales insights of Atliq Hardware LTD.
- Atliq Hardware is a manufacturing company which provides hardware peripherals to different clients, like Normad stores, Excel stores, Electronics store etc. all over India. 
- They have regional offices in diffrent states of the country.

The Problem Statement
======
- The problem statement here is, the Sales of the company are declining. The Sales Managing team is unable to recognize the factors affecting the Business. As it has different branches accross the country, the ower would like to know branch-wise performances of different cities, and in which city, they have to work more effectively to regain their sales number. 
- For that, as a member of Data Analysis team, we have to analyse the sales data of the company from different cities, and get insghts from the data to help make better business dicisions.
- We will first start with cleaning the dataset, removing unwanted data.
  
AIM's Grid
======
- The Aim's Grid is a very powerful tool and simultaneously really easy to use. 
- It helps yourself to be clear about what to do and it helps you to explain it to others as well.
- Missing information is visible at one glance and you can also see interdependencies in the different goal dimensions.
   
Data Discovery
======
We got the data od the company sales 

Data Analysis using SQL
======
1. SQL database dump is in db_dump.sql file above. Download `db_dump.sql` file to your local computer and import it as per instructions given in the tutorial video

### Data Analysis Using SQL

1. Show all customer records

    `SELECT * FROM customers;`

1. Show total number of customers

    `SELECT count(*) FROM customers;`

1. Show transactions for Chennai market (market code for chennai is Mark001

    `SELECT * FROM transactions where market_code='Mark001';`

1. Show distrinct product codes that were sold in chennai

    `SELECT distinct product_code FROM transactions where market_code='Mark001';`

1. Show transactions where currency is US dollars

    `SELECT * from transactions where currency="USD"`

1. Show transactions in 2020 join by date table

    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

1. Show total revenue in year 2020,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";`
	
1. Show total revenue in year 2020, January Month,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");`

1. Show total revenue in year 2020 in Chennai

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020
and transactions.market_code="Mark001";`

Data Cleaning and ETL in Tableau
======


Buliding Sales Dahboard 
======

Buliding Profit Analytics Dahboard 
======







