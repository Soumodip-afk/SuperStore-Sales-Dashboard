Super Store Sales Dashboard – Power BI Project



1. Project Overview

This project presents an interactive Super Store Sales Dashboard developed in Microsoft Power BI. The dashboard analyzes sales, profit, quantity, customer segments, product categories, sub-categories, payment methods, shipping modes, monthly trends, and regional/state-level performance.

The project is designed as an end-to-end business intelligence portfolio project, covering data preparation, calculated fields, interactive filtering, KPI reporting, and visual storytelling.

2. Project Objective

The main objective is to transform Super Store transaction data into an interactive dashboard that helps users:

Monitor total sales, profit, and quantity.

Compare performance across regions and states.

Analyze monthly sales and profit trends.

Understand category and sub-category contribution.

Compare payment methods and shipping modes.

Analyze customer segment performance.

Identify high-performing and loss-making areas.

Use interactive filters to explore the data from different business perspectives.

3. Dataset Description

The source dataset is an Excel workbook named SuperStore Sales DataSet.xlsx.

Dataset coverage

Attribute

Value

Rows / transactions

5,901

Date range

2019–2020

Unique orders

3,003

Unique customers

773

Unique products

1,755

Regions

4

Categories

3

Sub-categories

17

States

49

Sales

$1,565,804.32

Profit

$175,262.11

Quantity

22,317

Main fields

Order ID

Order Date

Ship Date

Ship Mode

Customer ID

Customer Name

Segment

Country

City

State

Region

Product ID

Category

Sub-Category

Product Name

Sales

Quantity

Profit

Returns

Payment Mode

4. Tools & Technologies

Tools

Microsoft Excel – source dataset

Microsoft Power BI Desktop – data modeling and dashboard development

Power Query – data preparation where required

DAX – calculated column / analytical logic

GitHub – project version control and documentation

Power BI techniques used

KPI cards

Donut charts

Area/line charts

Bar charts

Map visual

Slicers

Cross-filtering

Date hierarchy / time analysis

Calculated column

Aggregations such as SUM and AVERAGE

5. Data Preparation

The source Excel data was loaded into Power BI and prepared for analysis.

Key preparation steps include:

Loading the Excel dataset into Power BI.

Checking data types for dates, numeric fields, and categorical fields.

Using Order Date and Ship Date for delivery analysis.

Creating a delivery-duration calculated column.

Reviewing categorical fields such as Region, Category, Segment, Payment Mode, and Ship Mode.

Building visuals with appropriate aggregations.

Applying interactive filtering through the Region slicer.

Calculated column

The Power BI template contains the following calculated column:

AvgDelivery =
DATEDIFF(
    'Sheet1'[Order Date],
    'Sheet1'[Ship Date],
    DAY
)

This calculates the number of days between order date and ship date for each transaction. The dashboard displays the average of this field for the selected filter context.

Core analytical measures / aggregations

The dashboard uses standard Power BI aggregations such as:

Total Sales = SUM('Sheet1'[Sales])

Total Profit = SUM('Sheet1'[Profit])

Total Quantity = SUM('Sheet1'[Quantity])

Average Ship Days = AVERAGE('Sheet1'[AvgDelivery])

These can also be created explicitly as measures in the Power BI model for a more maintainable production-style implementation.

6. Dashboard Features

KPI Cards

Sales

Quantity

Profit

Average Ship Days

Sales Analysis

Sales by Payment Mode

Sales by Region

Sales by Segment

Sales by Category

Sales by Sub-Category

Sales by Ship Mode

Monthly Sales Trend

Profit Analysis

Monthly Profit Trend

Profit comparison across business dimensions

Geographic Analysis

Sales and Profit by State

Region-based filtering

Map visualization

Interactive Filtering

The dashboard includes a Region slicer with:

Central

East

South

West

Selecting a region updates the connected visuals.

7. Dashboard Snapshot – East Region

The supplied dashboard screenshot shows the East region selected.

KPI

Dashboard value

Sales

$450.23K

Profit

$53.40K

Quantity

6.25K

Average Ship Days

~4 days

For the East-region filter, the underlying dataset contains approximately $450.23K sales, $53.40K profit, and 6,251 units of quantity.

East-region observations

Consumer is the largest customer segment by sales in the selected region.

Office Supplies is the largest category by sales in the selected region.

Standard Class is the largest shipping mode by sales.

COD is the largest payment mode by sales.

Phones, Chairs, and Binders are among the leading sub-categories shown in the dashboard.

Monthly sales and profit vary considerably across the year, demonstrating the value of time-based analysis.

8. Overall Dataset Insights

Based on the source Excel data:

Regional sales

West: approximately $522.44K

East: approximately $450.23K

Central: approximately $341.01K

South: approximately $252.12K

Category sales

Office Supplies: approximately $643.71K

Technology: approximately $470.59K

Furniture: approximately $451.51K

Segment sales

Consumer: approximately $753.00K

Corporate: approximately $509.74K

Home Office: approximately $303.06K

Shipping mode

Standard Class contributes the largest share of sales at approximately $912.40K.

Payment mode

COD contributes approximately $667.42K in sales, followed by Online and Cards.

Profit observation

Technology generates approximately $90.46K profit, while Furniture generates approximately $10.01K. Some individual sub-categories and states show negative profit, making profitability analysis important rather than relying only on sales volume.

9. Business Questions Answered

The dashboard is designed to answer questions such as:

How much sales and profit are being generated?

Which region generates the most sales?

Which category contributes the most revenue?

Which sub-categories are the strongest contributors?

Which customer segment generates the most sales?

Which payment method is most commonly associated with sales?

Which shipping mode contributes the most sales?

How do sales change month by month?

How does profit change month by month?

Which states contribute strongly to sales and profit?

How many days does it take, on average, to ship orders?

How does regional performance change when the Region slicer is applied?

10. Dashboard Design

The dashboard uses a structured layout:

Header: project title and Region slicer

Left section: payment, regional, and segment analysis

Center section: KPI cards and monthly trend analysis

Right section: state map and product/shipping analysis

Bottom section: profit, category, and sub-category analysis

The design emphasizes quick KPI reading followed by detailed analysis.

11. Project Workflow

Excel Dataset
     ↓
Data Inspection
     ↓
Data Preparation
     ↓
Power BI Data Model
     ↓
Calculated Column / DAX
     ↓
Visual Development
     ↓
Slicers & Interactivity
     ↓
Dashboard Validation
     ↓
Business Insights
     ↓
Documentation
     ↓
GitHub Repository

10. Evaluation Criteria Mapping

Evaluation Area

Project Implementation

Workbook Design

Structured Excel source dataset

Formula & Functions

DAX calculated column and Power BI aggregations

Dashboard & Charts

KPI cards, charts, map, slicer and interactive visuals

Data Analysis

Sales, profit, quantity, category, region, segment and trend analysis

Automation

Power BI refresh-based reporting; no VBA macro is claimed

Documentation

README and project report

Presentation

Dashboard-based presentation

Creativity & Accuracy

Interactive layout, KPI-driven storytelling and validation against source data

11. Learning Outcomes

Through this project, the following skills were practiced:

Importing Excel data into Power BI

Understanding business datasets

Data type validation

Creating calculated columns

Applying DAX functions

Using Power BI aggregations

Building KPI cards

Creating interactive charts

Creating geographic visualizations

Using slicers and cross-filtering

Performing sales and profit analysis

Presenting business insights

Documenting a BI project

Preparing a GitHub portfolio repository

12. Limitations & Future Improvements

Possible future improvements include:

Creating a proper star-schema data model.

Adding dedicated Date, Customer, Product and Geography dimensions.

Creating explicit DAX measures instead of relying mainly on implicit aggregations.

Adding year-over-year growth measures.

Adding profit margin percentage.

Adding top/bottom customer analysis.

Adding top/bottom product analysis.

Adding return-rate analysis.

Adding drill-through pages.

Adding tooltip pages.

Adding dynamic titles.

Adding forecast analysis.

Adding a dedicated executive summary page.

Adding data-refresh documentation.

13. Conclusion

The Super Store Sales Dashboard converts transactional sales data into an interactive business intelligence solution. It provides a consolidated view of sales, profit, quantity, customer segments, product categories, shipping, payment methods, monthly trends, and geographical performance.

The project demonstrates the complete workflow from an Excel dataset to a Power BI dashboard and documented portfolio project.

14. Author

15. Soumodip Mondal.

    
