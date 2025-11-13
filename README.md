Banking Analytics Dashboard – End-to-End Data Project (Python • SQL • Power BI)

This project demonstrates a complete end-to-end data analytics workflow using Python, MySQL, and Power BI to analyze customer behavior, banking performance, and loan risk.
It integrates data engineering, EDA, SQL modeling, feature engineering, and BI dashboarding into one unified solution suitable for real-world analytics environments.

📌 Project Overview

The goal of this project is to build a comprehensive banking analytics system that helps stakeholders understand:

Customer demographics & segmentation

Loan distribution & risk factors

Deposit behavior & account usage patterns

Overall financial performance across customer groups

Key indicators used in risk analytics for banking and lending

The final outcome is an interactive multi-page Power BI dashboard powered by a clean relational data model and SQL-based calculations.

🧱 Architecture & Workflow
Excel Source File
      ↓
Python (Pandas, NumPy, Seaborn)
      ↓  Data Cleaning + EDA + Feature Engineering
MySQL Database (Structured Storage)
      ↓  SQL Queries + Aggregations
Power BI Desktop
      ↓  DAX Measures + KPIs + Interactive Dashboard
Final Analytics Insights

🛠️ Tech Stack
Layer	Tools
Programming & EDA	Python (Pandas, Matplotlib, Seaborn)
Database	MySQL Workbench / MySQL Server
BI Dashboard	Microsoft Power BI
Data Storage	CSV, SQL Tables
Visualization Design	Canva (for dashboard UI layout)
📂 Repository Structure
├── data/
│   ├── Banking.csv
│   ├── Banking System.sql
│
├── notebooks/
│   ├── Banking_EDA_Case_Study.ipynb
│   ├── banking_eda_case_study.py
│
├── dashboard/
│   ├── Banking Dashboard 2025.pbix
│   ├── visuals/ (dashboard screenshots)
│
├── presentation/
│   ├── Banking_Analytics_Advanced_Presentation.pptx
│
└── README.md

🔍 1. Data Preparation (Python)
Key Tasks Performed:

Imported raw Excel/CSV dataset

Handled missing values and inconsistent formats

Standardized categorical mappings (Gender, BRID, AdvisorID)

Feature engineered:

Income Band (Low, Mid, High) using pd.cut()

Year of Joining

Risk Indicators

Converted dataset into a SQL-ready structure

Validated data types and distributions

Sample Code:
bins = [0, 100000, 300000, float('inf')]
labels = ['Low', 'Mid', 'High']
df['Income_Band'] = pd.cut(df['Estimated_Income'], bins=bins, labels=labels)

📊 2. Exploratory Data Analysis

Performed both univariate and bivariate analysis:

Explored:

Numeric distributions (age, income, loan amounts)

Category-level patterns (nationality, relationship type, occupation)

Gender segmentation behavior

Loan vs deposit behavior

Correlation between financial attributes

Major Visuals:

Countplots for demographics

Histograms for income & loan distribution

Pairwise comparisons

Correlation heatmap for numeric attributes

Key Insights:

Strong positive correlation between bank deposits, savings, and checking accounts.

European customers make up the largest segment across all banking products.

Most customers hold one credit card; high-income customers show diversified financial activity.

Business lending and credit card balances significantly impact total loan exposure.

🗄️ 3. SQL Data Modeling

Cleaned data was stored into a MySQL database for:

Structured querying

Efficient aggregation

Use in Power BI as a live/refreshable data source

Example Query:
SELECT 
  Client_ID, Name, Estimated_Income, Bank_Loans, Bank_Deposit
FROM customer
WHERE Estimated_Income > 100000;

📈 4. Power BI Dashboard

The final dashboard consists of 4 fully interactive pages:

🔹 Home Page

Total Clients

Total Loan Exposure

Total Deposits

Savings & Checking Breakdown

Slicers:

Gender

Year of Joining

Navigation Buttons to other pages

🔹 Loan Analysis

Insights focused on risk, exposure, and loan distribution:

KPIs:

Bank Loan

Business Lending

Credit Card Balance

Visuals:

Loan by Income Band

Loan by Nationality

Loan by Occupation

Loan by Relationship Type

Filters:

Gender

Advisor

Relationship Category

🔹 Deposit Analysis

Behavior and deposit patterns:

KPIs:

Bank Deposit

Savings Account Total

Checking Account Total

Foreign Currency Holdings

Visuals:

Deposits by Income Band

Deposits by Nationality

Deposits by Relationship Type

🔹 Summary Page

Full consolidated view with:

All KPIs

Segmented insights

Customer behavior overview

Cross-filtered charts

📌 Business Impact

This project enables banking teams to:

Identify high-value and low-risk customer segments

Evaluate loan exposure across demographic groups

Detect patterns that influence creditworthiness

Understand cash flow across account types

Make data-driven lending decisions

🚀 How to Run This Project
1. Python Notebook
pip install pandas mysql-connector-python seaborn matplotlib

2. MySQL

Import Banking System.sql → create banking_case database → load table.

3. Power BI

Open Banking Dashboard 2025.pbix → update your MySQL credentials →

localhost
port: 3306
username: root
password: root
database: banking_case

👩🏽‍💻 Author

Kalkidan Bekele Argaw
Data Analyst • Python • SQL • Power BI • EDA
