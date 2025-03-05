# Machine Learning Credit Risk Classification

## Overview of the Analysis

In this analysis, we explored two machine learning models (Logistic Regression and Random Forest) to predict whether a loan is high-risk or healthy. The data used for this analysis is based on lending information, where the goal is to predict the loan status (`loan_status`), which can either be healthy (`0`) or high-risk (`1`).

### Variables:
- **loan_status (target variable)**: The label that indicates whether a loan is high-risk (`1`) or healthy (`0`).
- **loan_size**: The size of the loan requested by the borrower.
- **interest_rate**: The interest rate associated with the loan.
- **borrower_income**: The income of the borrower.
- **debt_to_income**: The ratio of the borrower’s debt to their income.
- **num_of_accounts**: The number of financial accounts the borrower has.
- **derogatory_marks**: The number of derogatory marks (e.g., late payments) on the borrower’s credit report.
- **total_debt**: The total amount of debt the borrower has.

### Machine Learning Process:
1. **Data Preprocessing**: The data was loaded, and the target variable (`loan_status`) was separated from the features.
2. **Train/Test Split**: The data was divided into training and testing sets to evaluate model performance.
3. **Modeling**: We used two algorithms—**Logistic Regression** and **Random Forest**—to build classification models.
4. **Evaluation**: Models were evaluated using accuracy, precision, recall, and F1-score.

### Algorithms Used:
- **Logistic Regression**: A linear model used for binary classification problems.
- **Random Forest**: A non-linear, ensemble model that uses multiple decision trees for classification.

## Results

- **Logistic Regression Model**:
    - **Accuracy**: 99%
    - **Precision (Healthy Loan - 0)**: 1.00
    - **Recall (Healthy Loan - 0)**: 0.99
    - **Precision (High-Risk Loan - 1)**: 0.84
    - **Recall (High-Risk Loan - 1)**: 0.94
    - **F1-Score (Healthy Loan - 0)**: 1.00
    - **F1-Score (High-Risk Loan - 1)**: 0.89

- **Random Forest Model**:
    - **Accuracy**: 99%
    - **Precision (Healthy Loan - 0)**: 1.00
    - **Recall (Healthy Loan - 0)**: 0.99
    - **Precision (High-Risk Loan - 1)**: 0.85
    - **Recall (High-Risk Loan - 1)**: 0.89
    - **F1-Score (Healthy Loan - 0)**: 1.00
    - **F1-Score (High-Risk Loan - 1)**: 0.87

## Summary

Both the **Logistic Regression** and **Random Forest** models performed exceptionally well, achieving an accuracy of **99%**. However, there are a few differences in how the models handle the high-risk loans:

- **Logistic Regression** achieved a slightly better **recall** for high-risk loans (94% vs. 89%) but slightly lower **precision** (84% vs. 85%).
- **Random Forest** achieved slightly higher **precision** for high-risk loans (85% vs. 84%) but had a lower **recall**.

### **Recommendation**:
- If minimizing false positives (i.e., incorrectly classifying healthy loans as high-risk) is more important, **Random Forest** would be the preferred model, as it has slightly better precision for high-risk loans.
- If it is more important to identify as many high-risk loans as possible (minimizing false negatives), **Logistic Regression** would be the better model due to its higher recall for high-risk loans.

In conclusion, both models are highly effective, and the choice of model depends on whether you prioritize precision or recall for high-risk loans. Given the overall performance, I would recommend starting with **Logistic Regression** for its better recall, but **Random Forest** could be an option if reducing false positives is a priority.
