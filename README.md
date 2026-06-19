# 🏦 Bank Customer Churn Analysis

## Project Overview
This is an independent, unguided project analyzing customer churn for a 
retail bank with 10,000 customers across France, Germany and Spain. 
The goal was to act as a data analyst and answer one core business 
question: why is the bank losing 1 in 5 customers?

All analysis was done in Excel using a full ETL pipeline, data modelling 
in Power Pivot, DAX measures and nested IF logic for customer segmentation.

## Business Problem
The bank is experiencing a 20.37% churn rate with 2,037 customers lost. 
Leadership needs to understand which customer segments are leaving, why 
they are leaving and what can be done about it.

## Dataset
- Source: Kaggle — Bank Customer Churn Dataset
- 10,000 customer records
- 12 variables including demographics, account details, 
  product holdings and churn status

## What I Built

### ETL Pipeline in Power Query
- Loaded raw CSV and cleaned column names
- Replaced 0/1 binary values with Yes/No for readability
- Built 5 custom segmentation columns as part of the automated pipeline:
  - Age Group (Young Adult / Adult / Middle Aged / Senior)
  - Balance Category (Zero Balance / Low / Medium / High)
  - Credit Score Category (Poor / Fair / Good / Very Good / Excellent)
  - Salary Tier (Very Low / Low / Medium / High)
  - Churn Risk Label (combining churn status, activity and balance)

### Data Model in Power Pivot
Loaded clean data into Power Pivot and built 7 DAX measures:
- Total Customers
- Total Churned Customers
- Churn Rate %
- Retention Rate %
- Average Credit Score
- Average Balance
- Average Age

### Customer Lookup Tool
Built an INDEX MATCH based lookup tool where you can enter any 
Customer ID and instantly pull all their details dynamically across 
the full dataset.

### 7 Pivot Table Reports
Each report built on DAX measures with conditional formatting and 
slicer filters:

| Report | Focus |
|---|---|
| Churn Overview | Headline KPIs across the full dataset |
| Churn by Country and Gender | Geographic and demographic breakdown |
| Churn by Age Group | Which life stage is most at risk |
| Churn by Credit Score | Whether financial risk drives churn |
| Churn by Products Held | Product level churn analysis |
| Churn by Activity Status | Impact of customer engagement on churn |
| Churn by Balance Category | Whether account balance predicts churn |

## Key Findings

**Finding 1: Germany is the crisis market**
Churn rate of 32.44%, double that of France and Spain. Female customers 
in Germany churn at 37.55%, the highest of any segment in the dataset.

**Finding 2: Middle Aged customers are walking out**
51.12% churn rate for customers aged 31 to 60. More than half of the 
bank's highest value segment has left.

**Finding 3: Product 3 and 4 are broken**
Product 3 has 82.71% churn (220 customers lost). Product 4 has 100% 
churn (60 customers). 93% of Product 4 churned customers are in the 
Adult or Middle Aged segments.

**Finding 4: Inactivity is a strong churn predictor**
Inactive members churn at 26.85% vs 14.27% for active members. 
Inactive customers hold slightly higher average balances, meaning the 
bank is losing valuable accounts not just low value ones.

**Finding 5: Zero balance customers are more loyal than expected**
Lowest churn at 13.82% while Medium balance customers churn at the 
highest rate of 24.29%. Challenges the assumption that higher balance 
means more loyalty.

**Finding 6: Credit score is not a churn driver**
Only 3.4% variation in churn rate across all credit score bands. 
Churn is driven by engagement and product gaps, not financial risk.

## Tools and Skills Used
| Tool | Purpose |
|---|---|
| Power Query | ETL pipeline, data cleaning, custom segmentation columns |
| Power Pivot | Data modelling and DAX measure creation |
| DAX | Custom KPI calculations across 7 measures |
| Nested IF Logic | Multi-condition customer segmentation |
| INDEX MATCH | Dynamic customer lookup tool |
| Pivot Tables | Report building across 7 business dimensions |
| Conditional Formatting | Visual churn rate indicators across all reports |

## Project File
📊 [Download Excel Workbook](your-github-file-link-here)
