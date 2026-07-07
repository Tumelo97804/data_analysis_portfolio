
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





# Mexico Real Estate Market Analysis Using Python

## Executive Summary

The purpose of this project was to analyze residential property listings in Mexico to understand the factors that influence housing prices. The analysis focused on cleaning the dataset, exploring its characteristics, visualizing relationships between variables, and identifying correlations between property size and price.

The findings indicate that larger properties generally command higher prices, although several outliers exist within the dataset. The distribution of property prices is positively skewed, meaning that while most properties are priced within the lower-to-middle range, a small number of luxury properties significantly increase the overall average.

This project demonstrates practical data analysis skills including data cleaning, exploratory data analysis (EDA), statistical analysis, and data visualization using Python.

---

# Business Problem

Real estate companies, investors, and property buyers require accurate information about market trends to make informed decisions. Understanding which property characteristics influence pricing enables stakeholders to:

* Set competitive property prices.
* Identify high-value investment opportunities.
* Understand market trends.
* Improve decision-making using data rather than assumptions.

This project aims to explore housing data and identify the variables most closely associated with property prices.

---

# Project Objectives

The objectives of this analysis were to:

* Import and inspect a real estate dataset.
* Clean and prepare the data for analysis.
* Explore the structure and quality of the dataset.
* Produce descriptive statistics.
* Visualize relationships between property area and price.
* Examine price distributions.
* Calculate correlations between numerical variables.
* Generate business insights and recommendations.

---

# Dataset Overview

The dataset contains residential property listings from Mexico.

Some of the variables included are:

* Property ID
* Property Title
* Description
* Property Type
* Country
* State
* Municipality
* Latitude
* Longitude
* Surface Covered (m²)
* Surface Total (m²)
* Price
* Price per Square Meter
* Currency
* Date Created

These variables allow the analysis of property characteristics and their relationship with market prices.

---

# Tools and Technologies

Programming Language

* Python

Libraries

* Pandas
* Matplotlib
* Seaborn
* Plotly Express

Development Environment

* Jupyter Notebook

---

# Methodology

## Step 1: Import Libraries

The project began by importing the required Python libraries for data manipulation and visualization.

Libraries used include:

* pandas
* matplotlib
* seaborn
* plotly

---

## Step 2: Load the Dataset

The housing dataset was imported into a Pandas DataFrame using:

```python
pd.read_csv()
```

The first five records were inspected to verify that the dataset loaded correctly.

---

## Step 3: Data Inspection

The dataset was explored using:

* head()
* info()
* shape
* describe()

This helped identify:

* Number of observations
* Number of variables
* Data types
* Missing values
* Summary statistics

---

## Step 4: Data Cleaning

Data cleaning included:

* Checking for missing values
* Removing duplicate records
* Renaming columns for readability

This ensured consistency before performing analysis.

---

# Exploratory Data Analysis

## 1. Descriptive Statistics

Summary statistics were calculated to understand the distribution of the numerical variables.

Metrics included:

* Mean
* Maximum
* Minimum
* Standard deviation

The project also calculated:

* Average Price per Square Meter
* Maximum Price per Square Meter
* Minimum Price per Square Meter

These statistics provide a quick overview of the housing market.

---

## 2. Scatter Plot

### Objective

Investigate the relationship between house size and price.

### Variables

X-axis

Surface Covered (m²)

Y-axis

Price per Square Meter

### Findings

The scatter plot suggests a positive relationship between property size and price.

Most larger properties tend to have higher prices, although the relationship is not perfectly linear.

Several outliers are visible, representing unusually expensive properties relative to their size.

Business Interpretation

Larger homes generally have higher market values, making property size one of the strongest pricing indicators.

---

## 3. Box Plot

### Objective

Detect outliers and examine the spread of housing prices.

### Findings

The box plot revealed:

* Presence of several extreme outliers
* Wide variation in property prices
* Uneven price distribution

Business Interpretation

Luxury properties create substantial variation in pricing. Analysts should investigate these separately because they may distort averages and predictive models.

---

## 4. Distribution Analysis

### Objective

Understand how property prices are distributed.

Histogram analysis shows that:

* Most houses are concentrated within lower and middle price ranges.
* High-priced luxury homes occur less frequently.
* The distribution is positively skewed.

Business Interpretation

Median prices are likely to represent the market better than the mean because the mean is influenced by expensive properties.

---

# Correlation Analysis

A correlation matrix was created using only numerical variables.

The project also calculated the correlation between:

* Price per Square Meter
* Surface Covered (m²)

### Findings

The correlation analysis indicates a positive relationship between property size and price.

The heatmap further illustrates how numerical variables relate to one another.

The strongest relationship observed is between property area and pricing variables.

Business Interpretation

Area is an important predictor of house prices and should be considered when building predictive pricing models.

---

# Key Insights

The analysis produced several important findings:

* Larger houses generally have higher prices.
* Property size is positively correlated with price.
* The housing market contains several high-priced outliers.
* Housing prices are positively skewed.
* Most listings fall within the lower-to-middle price range.
* Price per square meter varies considerably between properties.

---

# Business Recommendations

Based on the findings, the following recommendations are proposed:

### For Real Estate Agencies

Use property size as one of the primary variables when estimating selling prices.

### For Property Investors

Focus on neighborhoods where larger properties maintain relatively affordable prices to maximize investment potential.

### For Buyers

Compare properties using price per square meter instead of total price to obtain fairer comparisons.

### For Data Scientists

Develop predictive machine learning models using variables such as:

* Surface Covered
* Surface Total
* Property Type
* Municipality
* State

These variables are likely to improve price prediction accuracy.

---

# Limitations

The analysis has several limitations:

* Some missing values were present.
* Geographic variables were not fully explored.
* Only exploratory analysis was performed.
* No predictive model was developed.

---

# Future Work

Future improvements may include:

* Predicting house prices using Linear Regression.
* Building Random Forest or XGBoost models.
* Creating interactive dashboards using Tableau or Power BI.
* Performing geographic analysis using maps.
* Segmenting properties by city or municipality.
* Identifying market trends over time.

---

# Conclusion

This project successfully explored the Mexican housing market using Python.

The analysis demonstrated that property size is one of the most influential factors affecting house prices. Visualizations revealed clear pricing trends, highlighted outliers, and showed that the housing market is positively skewed.

Through data cleaning, exploratory data analysis, and correlation analysis, valuable insights were generated that can support pricing strategies, investment decisions, and future predictive modeling efforts.

---

# Skills Demonstrated

* Data Cleaning
* Data Wrangling
* Exploratory Data Analysis (EDA)
* Data Visualization
* Correlation Analysis
* Statistical Summary
* Python Programming
* Pandas
* Matplotlib
* Seaborn
* Plotly
* Jupyter Notebook

---

# Portfolio Summary

**Project:** Mexico Housing Market Analysis

**Objective:** Explore housing data to identify factors influencing property prices.

**Tech Stack:** Python, Pandas, Matplotlib, Seaborn, Plotly, Jupyter Notebook.

**Outcome:** Identified positive relationships between property size and price, detected pricing outliers, examined price distributions, and generated business recommendations that can support data-driven real estate decisions.



