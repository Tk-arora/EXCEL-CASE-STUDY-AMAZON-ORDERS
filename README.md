# EXCEL-CASE-STUDY-AMAZON-ORDERS

Welcome to the Excel Case Study documentation. This file outlines the steps and calculations used to analyze the provided data, including data cleaning, trend analysis, and sales target evaluation. Below are detailed explanations for each section of the case study:

---

## 1. Data Cleaning and Imputation

### a. Replacing Missing Values
- **Order Source**: Replaced missing values with the mode "Other" (imputed values are highlighted in color).
- **Customer Country**: Replaced missing values with the country having the most orders. A pivot table and chart were used to determine the mode (imputed values are highlighted in color).
- **Customer Age**: Missing ages were replaced with a moving average of the previous three data points using the formula:
  ```
  =IF(D2501="",AVERAGE(D2498:D2500),D2501)
  ```
  (Imputed values are highlighted in color).

### b. Finding Outliers
- **Order Value in Orders Table**:
  - Q1: 2364
  - Q3: 7439.25
  - IQR: 5075.25
  - Upper Bound: 15052.125
  - Lower Bound: -4233.825
  - Formula used: `=IF(OR(G2<$G$2508,G2>$G$2507),1,0)`
  - Result: No outliers detected.
- **Age Column in Customers Table**:
  - Q1: -36
  - Q3: -72
  - IQR: -36
  - Upper Bound: -126
  - Lower Bound: -18
  - Formula used: `=IF(OR(F2501<$F$2507,F2501>$F$2506),1,0)`
  - Result: No outliers detected.

---

## 2. Data Analysis

### a. Answers Sheet Calculations
- **Order Value and Count in the 2nd Half of the Year**:
  - Sum: 0
  - Count: 0
- **Order Value and Count for Indian Customers**:
  - Sum: 1,356,737
  - Count: 281
- **Average Order Value for Orders via WhatsApp**:
  - Average: 4760.823065
- **Count of Orders for Dates on or After 15 June 2023 and Age Over 30**:
  - Formula used: `=COUNTIFS(Orders!H2:H2501,">=15-06-2023",Orders!N2:N2501,">30")`
  - Result: 1083

### b. Sales Targets
- **Full Name Column**:
  - Created by combining first name and last name: `=B2 & " " & C2`
- **Orders Trend Analysis**:
  - Created a trend analysis for the number of orders and average value across months.
- **Order Trends by Country**:
  - Plotted a chart for the number of users and total order value by country.
- **Order Trends by Hour**:
  - Plotted trends for the most common hour for orders and highest average order value hour.
- **Orders by Day of Month**:
  - Plotted a trend for orders based on the day of the month.
- **Orders by Order Source**:
  - Plotted a trend showing the variation in the number of orders based on the order source.
- **Age Group Analysis**:
  - Identified age groups with the highest total order value and number of orders (age group 58-67).

### c. Sales Targets Evaluation
- **Sales Target Buckets**:
  - Defined categories: Target Not Met, Target Met, Exceeded Target, and plotted counts.
- **Sales Teams Targets**:
  - Plotted total sales targets for different sales teams.
- **Sales Manager Targets**:
  - Identified the sales manager with the highest target (Benjamin Chen: Target Not Met) and compared actual versus target.
- **Average Shortfall**:
  - Calculated average shortfall for Sales POCs who did not meet their targets: `=AVERAGE('Sales Targets'!I3:I93)` (Result: 21,703.52727)
- **Average % Target Reached**:
  - Calculated average percentage of the target reached by Sales Teams: 95%

### d. Customer Categories Insights
- **Youngest Category of Customers**:
  - Category D: Average Age: 52.986
- **Most Indian Males**:
  - Category A: 44 Indian males.

---

## 3. Final Steps

- **Save and Share the Excel File**: Ensure that all changes and analyses are saved. Share the file as required.

For any questions or further clarifications, please refer to the specific sections in the Excel file or contact the project lead.

--- 

Thank you for using this case study guide!
