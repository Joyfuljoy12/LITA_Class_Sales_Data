# LITA_Class_Sales_Data

### OUTLINE 
[Project Title](#project-title) 

[Project Overview](#project-overview) 

[Key Findings](#key-findings)

[Data Source](#data-source)

Methodology 

Data Cleaning and preparation

[Data Visualization](#data-visualization) 



### Project Title: Retail Sales Perfomance Data
-----
### Project Overview 
------
This Data Analysis project aims to generate insights into sales performance of a retail store over the previous and current year. By analysing the various parameters in the data received I explored sales data to gather/uncover key insights to make reasonable decisions.

### Key Findings
----
- Top-selling product
- Regional performance
- Monthly sales trends

### Data Source
---
The primary source of the Data used is LITA Capstone Project- Sales Data.xslx

#### Tools used/Methodology 
------
- Microsoft Excel [Download Here](https://www.microscoft.com)
  1. Data cleaning
  2. Analysis
  3. Visualization
- SQL- Structured Query Language
- Power BI- Power Business Intelligence for Data Visualization
- GitHub for Portfolio building

### Data cleaning and preparation 
----
Some basic action were taken, they include:
1. Data downloading from LMS (LITA- Data Analysis Class)
2. Data loading from each platforms such as Excel, SQL and Power BI
3. Data Inspection- Highlighting, inserting into tables and changing formatting or possible errors/blank space
4. Data Cleaning

#### Data Analysis
----
This is where we include some basic lines of code or queries and some DAX expressions used during the analysis;

-----Total sales for each product----
``` SQL
Select Sum (Total_sales) as TOTALSHIRT From [LITA Sales Data]
Where product = 'Shirt'
```

-----Number of sales transactions in each region-----
```SQL
select count (*) as TOTALSALESTRANSACTION from [LITA Sales Data]
where Region = 'south' and Product = 'shoes'
```

-----Top five highest-selling product----
```SQL
select top 5 * from [LITA Sales Data]
```

----Monthly sales transactions in each region---- 
```SQL
select Region,
      CASE
          WHEN Region IN ('North') then '1'
          WHEN Region IN ('South') then '2'
          WHEN Region IN ('East') then '3'
          Else '4'
End as RegionGroup,
sum(Total_Sales) as Totalsales from [LITA Sales Data]
where OrderDate in ('2024-04-01', '2024-04-30')
Group by Region
```
###### Note
From the sales data on SQL we have different region and product category, so from the queries provided one can insert a different region and product category to get desie result.


#### Data Visualization
----
![image](https://github.com/user-attachments/assets/76114807-3844-4268-ab34-72f47b8462ed)

![image](https://github.com/user-attachments/assets/526e23e5-25ff-4914-97a7-96c5115868b8)

![image](https://github.com/user-attachments/assets/059ae544-a09b-48b1-a67e-8b186a557c4b)

![image](https://github.com/user-attachments/assets/71bd7860-b94d-47ea-8b9c-94fee8a6e91a)

In Summary, 
      In the above diagrams, the top sales of product categories was shoes from region (south, east and west) during the year 2023 and 2024 at or almost a particular duration from February (2023), Quarter 1 to August (2023), Quarter 3 and also from February (2024), Quarter 1 to July (2024), Quarter 3. From this period, there is a change in the ecosystem causing the atmosphere to gradually change from harmattan weather to rainy weather. So therefore, individuals/ customers tend to make more purchase of shoes/sandals during this period.




to
