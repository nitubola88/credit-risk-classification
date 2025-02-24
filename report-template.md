## Overview of the Analysis

In this analysis, we built a model to predict loan default risks based on historical lending data. The dataset provides information about loan amounts, interest rates, borrower income, debt-to-income ratio, and other financial factors. The goal is to predict whether a loan is healthy (0) or high-risk (1) for default.

### Key Features:
- `loan_size`: The size of the loan.
- `interest_rate`: The loan's interest rate.
- `borrower_income`: The income of the borrower.
- `debt_to_income`: Debt-to-income ratio.
- `num_of_accounts`: Number of accounts held by the borrower.
- `derogatory_marks`: Negative marks on the borrower’s credit.
- `total_debt`: The total debt of the borrower.
 ## Results

* **Logistic Regression Model**:
  - **Accuracy**: 0.99
  - **Precision** (for high-risk loans): 0.84
  - **Recall** (for high-risk loans): 0.94

## Summary

The Logistic Regression model performed well with an accuracy of 99%. It correctly identified most healthy loans but did better with high-risk loans in terms of recall. However, precision for high-risk loans was lower (84%), indicating that some healthy loans were incorrectly classified as risky.

Based on this analysis, I recommend using the model as a first step. However, further improvement could be made by addressing class imbalance with resampling techniques or using alternative algorithms.

