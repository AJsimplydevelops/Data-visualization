# Project Report: Data Visualization
# Introduction
This project is to be able to report the hotel revenue to stakeholders. Obtaining data from database. Then manipulating the data on our SQL server so we can convey the information in a way that’s easy to understand. Then we connect that server to our Power BI so that we can visualize the data in a way that can communicate complex data relationships.

# Tasks
- Build a Database 
- Analyze and Retrieve Data with SQL 
- Connect Power BI to a Database 
- Visualize Data in Power BI

# Build Database
Using SQL server management studio, we inputted the following query:
with hotels as (
select * from dbo.[2018] 
union
select * from dbo.[2019] 
union
select * from dbo.[2020]) 
select * from hotels

left join dbo.market_segment
on hotels.market_segment = market_segment.market_segment
left join dbo.meal_cost
on meal_cost.meal = hotels.meal

# Visualize Data in Power BI
- After connecting Power BI to the database from the SQL server.
We implemented these various graphs that can convey the data, as this was a report of hotel revenue to relevant stakeholders:

![visualize-data](https://user-images.githubusercontent.com/78631693/236514265-32fcffcf-00f8-4ac3-a533-356a786dfbfe.PNG)
