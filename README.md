# UCI-Credit-Card-Risk-Report-and-Dashboard
End-to-end Power BI project: credit risk analysis with data transformation, custom DAX risk scoring, executive summary, and business insights.



 **Credit Risk Analysis Dashboard**

**Project Overview** :

This project analyzes the UCI Credit Card Default dataset to identify risk drivers, customer segments, and trends that influence credit defaults. The goal was to design an interactive Power BI dashboard that helps financial institutions monitor risk, profile customers, and recommend actionable strategies to reduce defaults.




 **Dataset**

Source: [UCI Machine Learning Repository – Default of Credit Card Clients Dataset]

Records: 30,000 customers

Key fields:

Demographics: Age, Gender, Education, Marriage

Credit Behavior: Limit Balance, Bill Amounts, Pay Amounts, Payment Status

Target Variable: DefaultFlag (1 = default, 0 = no default)








**1. Data Preparation**

Imported dataset into Power BI.

Cleaned nulls, renamed columns, created relationships.change datatypes of columns and cleansing other data. 

Created **AgeGroup** ,**RiskScore**,**DefaultFlag** and **CreditLimitDecile**.

Created Date Table for time-series analysis.

Derived calculated columns: AgeGroup, RiskScore buckets, Month Index.







**2. Measures & KPIs (DAX)**

DefaultRate = % of customers who defaulted.

RiskScore = heuristic combining delinquent months, pay history, utilization.

DelinquentMonths = count of months with delayed payments.

Aggregated KPIs for bill amount, pay amount, and limit utilization.






**3. Dashboard Pages**
**Page 1 – Portfolio Overview**

High-level KPIs: Default Rate, Avg Risk Score, Total Customers.

Slicers for Demographics (Gender, Education, Marriage).




**Page 2 – Risk Segments & Drivers**

Key Influencers (AI Visual): Shows drivers of default.

Decomposition Tree: Splits by Education, AgeGroup, PayStatus.

Bar Chart: Default Rate by Education & Marriage.

Top 10 Table: Highest risk customers (with drillthrough enabled).




**Page 3 – Customer Profile (Drillthrough)**

Select a customer → Drillthrough to profile page.

Cards: Customer Info, RiskScore.

Line Chart: Payment history (Bill vs Pay).
combo chart : Bill vs. Payment

Text Box: Recommended action based on RiskScore.







**Page 4 – Time Trends**

clustered column chart : DefaultRate by Month With Education

Area Chart: Total Bill vs Total Pay.





**Page 5 – Model & Recommendations (Storytelling)**

Key Findings, Recommendations, Limitations (text boxes).





**Key Findings**

Customers aged 21–30 are 2.5× more likely to default.

Low education segments show higher delinquency.

Customers with 3+ delinquent months have very high default risk.

Recent pay history is the strongest driver of default.




**Recommendations**

Manual review for RiskScore > 70 customers.

Lower initial limits for young customers; step-up only on good behavior.

Launch repayment plans & literacy programs for high-risk groups.

Regular monthly risk monitoring dashboards.





**Limitations**

Dataset is simulated (not real bank data).

Only covers 6 months of history.

RiskScore is heuristic — not ML-based.

Results not globally generalizable.







**Files in Repository**

UCI_Credit_Card_Risk_Dashboard.pbix → Main Power BI report.

README.md → This file.

UCI_Credit_Card_Risk_Dashboard-Executive_Summary.docx → 1-page narrative summary.


UCI_Credit_Card_Dataset.csv → Raw dataset (from UCI repo).







**How to Use**

Download the .pbix file.

Open in Power BI Desktop.

Use slicers/bookmark navigation to explore insights.

Drillthrough a customer ID for profile details.

Export findings (PDF / PPT) for stakeholders.
