# Data-Analyst-

## SQL Advanced Module Task
Task Description (Completed Work)

Collected and consolidated data to analyze account creation trends, user engagement with emails (including sends, opens, and clicks), and user behavior across key categories such as send intervals, account verification, and subscription status. The dataset enables cross-country activity comparisons, identification of key markets, and segmentation of users based on various behavioral and demographic parameters.

## Python for DA Module Task 
Project Overview

This project involved analyzing a global company's sales dataset, which includes transactions from both offline stores and online channels. The goal was to clean, process, and analyze the data to extract valuable business insights.
The dataset consists of three tables:
events.csv — sales transactions over multiple years
products.csv — product categories and their codes
countries.csv — country and region information with corresponding codes
The main objective was to clean the data and perform a comprehensive analysis to uncover key performance metrics and actionable insights for the business.

Project Workflow
1. Data Overview
Loaded and explored the datasets to understand column contents, data types, and structure.
Identified key fields for merging the three tables.
Created initial descriptive statistics to summarize data coverage and distribution.

2. Data Cleaning
Checked for missing values in each table, assessed their proportion, and investigated potential causes.
Imputed or removed missing values with proper justification.
Verified and corrected data types where necessary (e.g., converting date columns to datetime format).
Detected and handled duplicates, considering whitespace, letter casing, and potential Cyrillic/Latin character inconsistencies.
Investigated anomalies and outliers in the data to ensure reliability for analysis.

3. Data Analysis and Visualization
Merged the three tables into a single dataframe and removed unnecessary columns for analysis.
Renamed columns where needed for clarity.
Key metrics calculated and visualized include:
Total number of orders
Total profit and revenue
Average order value
Total units sold
Number of countries and regions covered
Average shipping duration
Other custom KPIs relevant to business performance
Analysis performed across multiple dimensions:
Product Categories: revenue, costs, profit, popularity
Geography: performance by country and region
Sales Channels: online vs offline
Shipping Duration: analysis of time between order and shipment by product category, country, and region
Profit Dependency: examined whether profit correlates with shipping duration
Time Dynamics: analyzed sales trends over time by category, country, and region
Day-of-Week Analysis: identified patterns in sales by day of the week
Seasonality: evaluated potential seasonal trends in product sales using heatmaps

4. Reporting
Compiled a detailed report in Google Colab, including:
Fully documented code
Interactive and static visualizations
Business-focused explanations and insights
Generated actionable conclusions to guide decision-making in sales, marketing, and logistics.
Key Deliverables
Google Colab notebook with cleaned datasets, analysis, visualizations, and explanations
Business insights summary highlighting top product categories, key markets, profitable channels, shipping patterns, and seasonal trends
Interactive charts and heatmaps for clear representation of sales performance and trends

This project demonstrates end-to-end Data Analytics skills, including data cleaning, transformation, analysis, visualization, and reporting, suitable for showcasing in a portfolio or resume.

# **Portfolio Project 1.ipynb**
## E-Commerce Sales Analysis
### **Project Overview**

This project provides a comprehensive analysis of an e-commerce dataset to uncover insights into sales performance, user behavior, product trends, and traffic sources. Using SQL, Python, and Tableau, the analysis covers both descriptive and statistical approaches to support business decision-making.

Key Goals:
1.Extract and clean data from Google BigQuery.
2.Explore sales trends, top-selling products, and high-performing regions.
3.Analyze user behavior (registered vs unregistered users).
4.Examine traffic sources, device types, and session dynamics.
5.Conduct statistical tests to validate hypotheses.
6.Visualize insights with interactive dashboards.

###**Data Sources**

The dataset is stored in Google BigQuery and contains the following tables:

Table Name	Description
session	User sessions, including session IDs and dates.
order	Orders placed during each session.
product	Product catalog with categories, names, prices, and descriptions.
session_params	Additional session metadata: device, browser, country, traffic source, etc.
account	Registered users’ information: email verification, subscription status.
account_session	Links sessions to registered accounts.

Other supporting tables include email_sent, email_open, email_visit, event_params, paid_search_cost, ab_test, and revenue_predict.

### **Technologies**
**Python** (Pandas, NumPy, Matplotlib, Seaborn, SciPy, Statsmodels)
**SQL** (Google BigQuery)
**Tableau** (for dashboards and interactive visualizations)
**Google Colab** (for running Python notebooks)

### **Project Structure**
**Data Extraction & Cleaning**
Load data from BigQuery.
Merge tables to create a unified dataset.
Handle missing values and correct data types.
**Exploratory Data Analysis (EDA)**
Overview of sales trends over time.
Top regions, countries, and continents by sales and orders.
Top products and categories.
Traffic source and device distribution.
**Sales Dynamics & User Behavior**
Comparison of registered vs unregistered users.
Average order value (AOV) by device type.
Organic traffic share by region.
**Statistical Analysis**
Correlations between sessions and sales.
Correlations between top product categories and traffic channels.
Group comparisons (registered vs unregistered, desktop vs mobile).
Tests used: Mann–Whitney U, Welch’s t-test, KS test, ANOVA, Chi-square test.
**Visualizations**
Line charts, bar charts, and heatmaps for sales, traffic, and product performance.
Comparative distributions and correlation matrices.
**Dashboards**
Interactive Tableau dashboards showing sales trends, top categories, and regional insights.


### **Key Insights**
**Top Regions**: Americas, Europe, and Asia drive the majority of sales.
**User Segmentation**: Registered users contribute significantly higher sales; ~72% verified emails.
**Product Performance**: Certain product categories show synchronized demand, enabling cross-selling opportunities.
**Traffic Sources**: Organic and direct channels are the largest contributors to sessions and sales.
**Device Analysis:** No significant difference in AOV between desktop and mobile users.
**Temporal Patterns**: Daily sales strongly correlate with session volumes (r ≈ 0.96).
### **Business Recommendations:**
Focus marketing on high-performing channels and regions.
Encourage user registration to boost verified customer base.
Explore cross-selling based on correlated product categories.
Optimize mobile and desktop experience for engagement.
How to Run the Project
Open the Jupyter notebook in Google Colab.
Connect to Google BigQuery with your credentials.
Run cells sequentially to extract data, perform analysis, and generate visualizations.
Export results or dashboards to Tableau Public for interactive exploration.


# Portfolio Project 2
## A/B Testing Statistical Significance Tool
### Project Overview

This project implements an end-to-end A/B testing analysis pipeline using Python and Tableau.
The main goal is to calculate statistical significance for multiple funnel metrics without relying on online calculators and to prepare a clean, visualization-ready dataset for dashboarding.

The solution is scalable, metric-agnostic, and designed to support multiple tests and segmentation dimensions (test ID, country, device, channel, etc.).
### Metrics Analyzed
1. add_payment_info / session
2. add_shipping_info / session
3. begin_checkout / session
4. new account / session

### Statistical Methodology
Test Used
Two-proportion z-test

Library
statsmodels.stats.proportion.proportions_ztest
Z-Statistic Convention

Statistical Significance Criteria
Significance level: α = 0.05
Two-sided test
Result is considered statistically significant if:
p_value < 0.05
### Tableau Dashboard

The final table is used to build a Tableau dashboard that:

Compares control vs test performance
Highlights statistically significant results
Applies conditional formatting based on p-value
Displays metric uplift and direction
Formatting Logic

p_value < 0.05 → black text
p_value ≥ 0.05 → red text

# Author
# Anastasiia Yakhiaieva
