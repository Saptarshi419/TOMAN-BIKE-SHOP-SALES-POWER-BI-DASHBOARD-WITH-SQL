Dashboard Preview:
![image](https://github.com/user-attachments/assets/dca4c3c3-b863-4c26-9b98-e2eb1771a051)
Page 1

![image](https://github.com/user-attachments/assets/1ea141da-7ea4-48b6-ab8a-e442d8e4db0f)
Page 2

Overview:

To Develop a Power BI Dashboard for “Toman Bike Shop Sales” that displays key performance metrics for informed decision-making.

Requirements: 

1)	Hourly Revenue Analysis
2)	Profit and Revenue Trends
3)	Seasonal Revenue
4)	Rider Demographics

Data Analysis Workflow:

1)	Create Database
2)	Develop SQL Queries
3)	Connect to Power BI to DB
4)	Build a Dashboard in Power BI
5)	Answer the Analysis Question

Data Analysis in MS SQL Server:

First, I have created a database in MS SQL Server in the name of Bike Share DB
Then .csv flat files has been connected to the database and fired the following quarry to extract the insights from the data.
with cte as (
select * from bike_share_yr_0
union all
select * from bike_share_yr_1)


select
dteday,
season,
a.yr,
weekday,
hr,
rider_type,
riders,
price,
COGS,
riders*price as revenue,
riders*price -COGS*riders as profit
from cte a
left join cost_table b
on a.yr = b.yr


![image](https://github.com/user-attachments/assets/4e022ad6-c0b1-45df-87fb-1c6651edd19b)

The table displays hourly sales data across a week, with higher earnings in midday and early evening hours, particularly around 10 to 15 hours, suggesting these are the most profitable times.
Days like Wednesday and Friday show notably higher sales, indicating variable profitability across the week.


Project Stages:

1.	Requirement Gathering: Understanding the key requirement.
2.	Data Walkthrough: Understand data structure and quality.
3.	Creating Database: Creating a database in MS SQL Server
4.	Data Connection To DB: Import the flat file to the DB.
5.	SQL Querry: Writing SQL Querry to extract insights.
6.	Data Connection: Connect Power BI to data sources.
7.	Data Modeling: Structure data for analysis.
8.	Data Processing: Prepare data for visualization.
9.	Dashboard Layout: Design a user-friendly interface.
10.	Charts Development: Develop and format visualizations.
11.	Dashboard Development: Integrate components into a dashboard.
12.	Insights Generation: Analyze data to generate insights.


Key Visualizations:

Sum of Revenue: It shows the sum of total revenue.
Sum of Profit: It shows the sum of total profit.
Hourly Revenue Analysis: A Line Chart contains the hourly revenue analysis with respect of riders, avg of revenue & avg of profit.
Revenue By Season: A bar chart showing the revenue by season
Sum of Riders By Rider Type: A Pie Chart that showing the sum of riders by rider type.
Analysis & Recommendation: Analysis of the price for years 2021 and 2022. And recommendation if price should be increased or not.


KPIs:

Hourly Revenue Analysis
Sum of Revenue
Sum of Profit
Seasonal Revenue
Total Riders by Rider Type


Key Insights:

1) If the price in 2022 was $4.99, a 10% increase would make the new price about $5.49.
2) A 15% increase would set the price at approximately $5.74.



