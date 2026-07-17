Banking Business Intelligence Dashboard
A Power BI capstone project analyzing customer, transaction, loan, credit card, and risk data from a banking dataset of 5,000 customer records. The dashboard is built across eight report pages, each covering a distinct area of banking operations, from a high-level executive summary down to detailed risk and feedback analysis.

Project Overview
This project demonstrates an end-to-end business intelligence workflow: cleaning a raw banking dataset, designing a relational data model, writing custom DAX measures, and building an interactive, multi-page Power BI report intended for both executive and operational audiences.

Dashboard Pages
Executive Overview - High-level KPIs summarizing customers, accounts, deposits, withdrawals, and transactions
Customer Analytics - Customer demographics and account-level insights
Transaction Analytics - Transaction volume, type, and trend analysis
Loan Portfolio - Loan amounts, interest rates, approval and rejection analysis
Credit Card Analytics - Credit limit, utilization, and rewards analysis
Risk and Anomaly Analytics - Flagged transactions and anomaly monitoring
Customer Experience - Feedback categorization and complaint resolution tracking
Business Insights - Summary findings and recommendations derived from the analysis


Tools Used
Power BI Desktop for data modeling, visualization, and report design
DAX for all custom measures and calculations
CSV as the source data format


Repository Structure

banking-capstone-dashboard/
├── README.md
├── Banking_Capstone_Dashboard.pbix
├── data/
│   └── Banking_Capstone_Cleaned_Dataset.csv
├── docs/
│   └── DAX_measures.md
└── screenshots/
    ├── 01_executive_overview.png
    ├── 02_customer_analytics.png
    ├── 03_transaction_analytics.png
    ├── 04_loan_portfolio.png
    ├── 05_credit_card_analytics.png
    ├── 06_risk_anomaly_analytics.png
    ├── 07_customer_experience.png
    └── 08_business_insights.png

Key DAX Measures
A full list of measures used across the report is documented in docs/DAX_measures.md. Core measures include Total Customers, Total Deposits, Total Withdrawals, Net Balance, Total Loan, Average Loan, Total Credit Limit, Average Credit Utilization, Rewards Points, Anomalies, Complaint Count, and Resolved Rate.

Key Insights
Customer feedback is evenly distributed across Complaint, Praise, and Suggestion categories, with no single category dominating overall sentiment.
The top ten cities account for a disproportionate share of transaction volume and rewards activity, indicating concentrated customer engagement in specific regions.
The loan approval rate is approximately 34 percent, suggesting an opportunity to review approval criteria or applicant qualification support.
Average credit utilization sits at approximately 63 percent, indicating moderate to high reliance on credit among customers.
Only about half of customer complaints are marked as resolved, highlighting room to improve complaint resolution turnaround.
Anomaly flags are concentrated among a specific subset of cities, which may indicate localized patterns worth further investigation.


How to Use
Clone or download this repository.
Open Banking_Capstone_Dashboard.pbix in Power BI Desktop.
Use the filters on each page to explore the data by city, account type, loan status, card type, feedback type, and other dimensions.
Refer to the screenshots folder for a static preview of each page without opening Power BI.


Author
Tushan Pandey
https://www.linkedin.com/in/tushan-pandey-172934246/ 
