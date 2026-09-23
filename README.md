# Customer Churn Analysis

**Created by:** Rahul Yadav\
**Role:** Aspiring Data Analyst

## Project Overview

Customer Churn Analysis is a data analysis project that explores
customer behavior and identifies factors associated with customer churn.

The project uses customer, subscription, and support data to clean,
analyze, visualize, and generate business insights using Python and SQL.

## Business Problem

Customer churn can directly impact recurring revenue and customer
lifetime value.

This project analyzes customer demographics, subscription details,
contract types, monthly charges, Customer Lifetime Value (CLTV), churn
scores, and customer support interactions to understand churn patterns.

## Objectives

-   Analyze customer churn patterns
-   Identify factors related to customer churn
-   Perform data cleaning and preprocessing
-   Explore customer demographics and subscription behavior
-   Analyze customer support interactions
-   Analyze revenue at risk
-   Create visualizations for business analysis
-   Generate business insights and recommendations

## Dataset & Database Structure

The project uses a SQLite database containing three related tables:

  ------------------------------------------------------------------------
  Table                                         Rows Description
  --------------------- ---------------------------- ---------------------
  Customer                                       600 Customer demographic
                                                     and basic information

  Subscription                                   600 Subscription, plan,
                                                     contract, charges,
                                                     and churn-related
                                                     information

  Support                                      1,000 Customer support
                                                     interactions,
                                                     escalations, and CSAT
                                                     information
  ------------------------------------------------------------------------

The common key used to integrate the tables is `customerid`.

**Relationship:** Customer → Subscription → Support

## Tools & Technologies

-   Python
-   SQL
-   Pandas
-   NumPy
-   Matplotlib
-   Seaborn
-   SQLite
-   Jupyter Notebook

## Data Cleaning

The project includes:

-   Checking dataset shape and column information
-   Checking missing values
-   Checking duplicate records
-   Renaming columns
-   Removing unnecessary columns
-   Converting date columns to datetime
-   Standardizing gender values
-   Preparing customer, subscription, and support data for analysis

Missing cancellation dates and cancellation reasons are retained because
they correspond to customers without recorded cancellations.

## Data Integration

Customer and subscription data are integrated using `customerid`.

Support information is integrated while retaining customers who do not
have a recorded support interaction.

The resulting integrated dataset contains **600 customer-level
records**.

## Feature Engineering

The project creates analytical features including:

-   `churn_flag`
-   `age`
-   `age_group`
-   `complaint_count`
-   `churn_risk`
-   `cancellation_month`
-   `support_interaction`

### Churn Flag

-   `1` → Customer churned
-   `0` → Customer remains active

### Churn Risk

Based on the existing `churn_score`:

-   **Low:** score \< 50
-   **Medium:** 50--69
-   **High:** ≥ 70

## Exploratory Data Analysis

### Customer Analysis

-   Customer distribution by state
-   Customer distribution by gender
-   Customer distribution by age group
-   Age group vs churn rate

### Subscription Analysis

-   Subscription type distribution
-   Plan type distribution
-   Contract type distribution
-   Plan type vs churn rate
-   Contract type vs churn rate
-   Monthly charges analysis
-   CLTV analysis

### Support Analysis

-   Support interaction distribution
-   Escalation analysis
-   CSAT score analysis
-   Support interaction vs churn
-   Support interaction count vs churn

### Churn Analysis

-   Overall churn rate
-   Churn by gender
-   Churn by state
-   Churn by age group

### Revenue Analysis

-   Monthly revenue by state
-   Revenue at risk due to churn

### Time-Based Analysis

-   Monthly churn trend

## Key Business Insights

### Overall Churn

-   **22.33%** of customers have churned.
-   **77.67%** remain active.

### Plan Type

-   Standard: **25.99%** churn rate
-   Premium: **23.85%**
-   Basic: **18.11%**

### Contract Type

-   Monthly: **23.54%** churn rate
-   Annual: **20.27%**

### Age Group

-   61--70: **31.17%** churn rate
-   51--60: **15.15%**
-   Other age groups: **22.39%--23.53%**

### Gender

-   Male: **22.90%**
-   Female: **21.72%**

### State

-   Jharkhand and Odisha: **33.33%**
-   Gujarat: **0.00%**
-   Rajasthan: **32.00%**

### Support Interaction

-   1 recorded support interaction: **24.01%** churn rate
-   No recorded support interaction: **18.88%**
-   Difference: **5.13 percentage points**

> "No recorded support interaction" refers to the available support
> records in this dataset; it does not necessarily mean the customer
> never contacted support.

### Revenue at Risk

-   Total monthly revenue: **₹11,643.95**
-   Revenue associated with churned customers: **₹2,778.29**
-   Revenue at risk: **23.86%**

### Monthly Churn

Monthly churn fluctuates between **1 and 6 customers**, with several
months showing higher cancellation counts.

## Business Recommendations

1.  Monitor customer segments with higher observed churn rates.
2.  Investigate higher churn among Standard-plan customers.
3.  Monitor Monthly-contract customers and analyze cancellation reasons.
4.  Review recurring customer support issues and escalation patterns.
5.  Monitor monthly revenue associated with churned customers.
6.  Track churn trends over time.
7.  Compare churn scores with actual churn outcomes.
8.  Build a churn monitoring dashboard with Churn Rate, Active
    Customers, Churned Customers, Revenue at Risk, Monthly Churn,
    Monthly Charges, CLTV, Support Interactions, CSAT Score, and Churn
    Risk.

## Project Workflow

``` text
SQLite Database
      ↓
Data Loading
      ↓
Data Understanding
      ↓
Data Cleaning
      ↓
Data Integration
      ↓
Feature Engineering
      ↓
Exploratory Data Analysis
      ↓
Churn Analysis
      ↓
Revenue Analysis
      ↓
Business Insights
      ↓
Recommendations
```

## Conclusion

This project provides a data-driven view of customer churn using
customer, subscription, and support data.

The analysis identifies churn patterns across plan type, contract type,
age group, gender, state, and customer support interactions. It also
estimates the monthly revenue associated with churned customers.

The project demonstrates practical use of **SQL, Python, Pandas, NumPy,
Matplotlib, and Seaborn** to transform customer data into business
insights and actionable recommendations.

## Author

**Rahul Yadav**\
Aspiring Data Analyst\
B.Tech CSE (Data Science)

**Skills:** Python \| SQL \| Pandas \| NumPy \| Matplotlib \| Seaborn

