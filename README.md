
Superstore Sales Analysis (2014–2017)
Google Data Analytics Case Study (Ask → Prepare → Process → Analyze → Share → Act)
________________________________________
ASK
Business Problem
The company sells products across multiple cities, states, and regions in the United States (2014–2017). Despite strong sales activity, the business is experiencing losses and inconsistent profitability.
Objective
Analyze sales performance to identify:
•	Performance differences by city, state, and region
•	Best and worst performing regions
•	Most profitable products
•	Impact of discounts on profit
•	Customer segments with highest spending
•	Year with highest sales
•	Effect of shipping method on profit
________________________________________
PREPARE
Data Source
•	Dataset: Superstore Sales Data (2014–2017)
•	Format: CSV file
•	Tool used: Microsoft Excel
Data Setup
To ensure safe and structured analysis:
•	Converted .csv file to .xlsx
•	Created separate sheets:
o	Working Sheet → raw working data
o	Pivot Tables → analysis outputs
o	Dashboard → visualizations
Data Cleaning & Standardization
Renamed columns for consistency:
•	Row ID → Row_ID
•	Order ID → Order_ID
•	Order Date → Order_Date
•	Ship Date → Ship_Date
•	Ship Mode → Ship_Mode
•	Customer ID → Customer_ID
•	Customer Name → Customer_Name
•	Postal Code → Postal_Code
•	Product ID → Product_ID
•	Sub-Category → Sub_Category
•	Product Name → Product_Name
Data Validation
•	Verified correct data types:
o	Dates → Date format
o	Sales, Profit, Discount → Numeric/Currency
o	Quantity → Number
________________________________________
PROCESS
Data Cleaning Steps
•	Removed duplicate records(none found)
•	Checked for missing values (none found)
•	Filtered blank cells using Excel filters
•	Standardized formatting across key columns:
o	Sales → Currency format
o	Profit → Currency format
o	Discount → Numeric format
o	Quantity → Whole number format
Feature Engineering
Created a new column:
Profit_Category
=IF(U2<0,"No Profit","Profit")
This helped classify transactions into:
•	Profit-making sales
•	Loss-making sales
________________________________________
ANALYZE
Pivot Table Analysis
1. Sales Performance by Region, State, and City
•	Compared total sales  across states and cities
•	Identified top-performing and underperforming areas
2. Regional Performance
•	West region generated significantly higher revenue and profit
3. Product Profitability
•	Some product categories generated the highest profits
•	Others contributed to frequent low-profit or loss-making sales
4. Discount Impact
•	Discounts above 30% (0.30) were strongly linked to losses
•	Transactions without discounts generated the highest profits
6. Yearly Sales Trend
•	2017 recorded the highest sales
•	2018 had the lowest sales 
7. Shipping Mode Analysis
•	Shipping method had no significant negative impact on profit
•	Standard Class shipping contributed the highest total profit due to volume
________________________________________
 SHARE (Dashboard)
Dashboard Components
•	Pivot charts for:
o	Sales and Profit by region
o	States and cities total sales
o	Discount vs profit relationship
o	Shipping mode performance
o	Yearly sales trend
o	Product sales and profit
Enhancements
•	Removed gridlines for cleaner visuals
•	Added slicers for:
o	Region
o	Year

These allow interactive filtering of insights.
________________________________________
ACT (Business Recommendations)
Based on the analysis:
1. Control Discounts
•	Avoid discounts above 30%
•	High discounts directly reduce profitability
2. Improve Low-Performing Regions
•	Investigate weak regions
•	Adjust marketing or product focus
3. Focus on High-Profit Products
•	Prioritize inventory and promotion of high-margin products
4. Optimize Customer Targeting
•	Focus on high-spending customer segments for marketing campaigns
5. Maintain Shipping Strategy
•	No urgent changes required to shipping methods
•	Standard shipping remains cost-effective due to volume efficiency
________________________________________
Final Note
This project demonstrates an end-to-end data analysis workflow using Excel, applying structured business thinking to real-world retail data.
________________________________________

