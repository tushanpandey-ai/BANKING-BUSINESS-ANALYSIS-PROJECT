# DAX Measures

## Executive Overview

```
Total Customers = DISTINCTCOUNT('Banking_Capstone_Cleaned_Dataset'[Customer_ID])

Total Accounts = DISTINCTCOUNT('Banking_Capstone_Cleaned_Dataset'[Customer_ID])

Total Deposits =
CALCULATE(
    SUM('Banking_Capstone_Cleaned_Dataset'[Transaction_Amount]),
    'Banking_Capstone_Cleaned_Dataset'[Transaction_Type] = "Deposit"
)

Total Withdrawals =
CALCULATE(
    SUM('Banking_Capstone_Cleaned_Dataset'[Transaction_Amount]),
    'Banking_Capstone_Cleaned_Dataset'[Transaction_Type] = "Withdrawal"
)

Net Balance = SUM('Banking_Capstone_Cleaned_Dataset'[Account_Balance])

Average Balance = AVERAGE('Banking_Capstone_Cleaned_Dataset'[Account_Balance])

Transactions = COUNT('Banking_Capstone_Cleaned_Dataset'[TransactionID])

Average Transaction = AVERAGE('Banking_Capstone_Cleaned_Dataset'[Transaction_Amount])

Anomalies =
CALCULATE(
    COUNTROWS('Banking_Capstone_Cleaned_Dataset'),
    'Banking_Capstone_Cleaned_Dataset'[Anomaly] = 1
)
```

## Customer Analytics

```
Average Age = AVERAGE('Banking_Capstone_Cleaned_Dataset'[Age])

Total Cities = DISTINCTCOUNT('Banking_Capstone_Cleaned_Dataset'[City])

Total Branches = DISTINCTCOUNT('Banking_Capstone_Cleaned_Dataset'[Branch_ID])
```

## Transaction Analytics

```
Max Transaction = MAX('Banking_Capstone_Cleaned_Dataset'[Transaction_Amount])

Min Transaction = MIN('Banking_Capstone_Cleaned_Dataset'[Transaction_Amount])
```

## Loan Portfolio

```
Total Loan = SUM('Banking_Capstone_Cleaned_Dataset'[Loan_Amount])

Average Loan = AVERAGE('Banking_Capstone_Cleaned_Dataset'[Loan_Amount])

Avg Loan to Balance Ratio = AVERAGE('Banking_Capstone_Cleaned_Dataset'[Loan_to_Balance_Ratio])

Approval Rate =
DIVIDE(
    CALCULATE(COUNTROWS('Banking_Capstone_Cleaned_Dataset'), 'Banking_Capstone_Cleaned_Dataset'[Loan_Status] = "Approved"),
    COUNTROWS('Banking_Capstone_Cleaned_Dataset')
)
```

## Credit Card Analytics

```
Total Credit Limit = SUM('Banking_Capstone_Cleaned_Dataset'[Credit_Limit])

Avg Credit Utilization =
AVERAGEX(
    'Banking_Capstone_Cleaned_Dataset',
    DIVIDE('Banking_Capstone_Cleaned_Dataset'[Credit_Card_Balance], 'Banking_Capstone_Cleaned_Dataset'[Credit_Limit])
)

Rewards Points = SUM('Banking_Capstone_Cleaned_Dataset'[Rewards_Points])
```

## Risk and Anomaly Analytics / Customer Experience

```
Complaint Count =
CALCULATE(
    COUNTROWS('Banking_Capstone_Cleaned_Dataset'),
    'Banking_Capstone_Cleaned_Dataset'[Feedback_Type] = "Complaint"
)

Resolved Rate =
DIVIDE(
    CALCULATE(COUNTROWS('Banking_Capstone_Cleaned_Dataset'), 'Banking_Capstone_Cleaned_Dataset'[Resolution_Status] = "Resolved"),
    COUNTROWS('Banking_Capstone_Cleaned_Dataset')
)
```
