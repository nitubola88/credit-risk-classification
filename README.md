# Credit Risk Analysis Report

## Overview of the Analysis

The purpose of this analysis is to assess the credit risk of loans by using historical lending data from a peer-to-peer lending service. We aim to build a machine learning model that can classify loans as either healthy (label 0) or high-risk (label 1) based on various features. This model will help the company in determining the creditworthiness of borrowers and in managing loan risk more effectively.

### Key Steps:
- **Data Preprocessing**: The dataset was cleaned and split into features (`X`) and labels (`y`), with `loan_status` being the target label.
- **Model Training**: A logistic regression model was trained using the training data.
- **Model Evaluation**: The model's performance was evaluated using a confusion matrix and classification report, providing metrics such as accuracy, precision, recall, and F1-score.

---

## Results

Here are the key metrics from the classification report for the logistic regression model:

- **Accuracy**: 99%
  - The model correctly predicted the loan status (healthy or high-risk) 99% of the time.
  
- **Precision (Healthy Loan - 0)**: 1.00
  - The model predicted healthy loans with 100% accuracy.
  
- **Recall (Healthy Loan - 0)**: 0.99
  - The model correctly identified 99% of all healthy loans.
  
- **Precision (High-Risk Loan - 1)**: 0.84
  - The model predicted high-risk loans with 84% accuracy.
  
- **Recall (High-Risk Loan - 1)**: 0.94
  - The model correctly identified 94% of all high-risk loans.
  
- **F1-Score (High-Risk Loan - 1)**: 0.89
  - The model balanced precision and recall effectively for high-risk loans.

### Confusion Matrix:



          precision    recall  f1-score   support

       0       1.00      0.99      1.00     18765
       1       0.84      0.94      0.89       619

accuracy                           0.99     19384


---

## Summary

The logistic regression model demonstrates excellent performance in predicting both healthy loans (`0`) and high-risk loans (`1`).

- **For healthy loans**, the model performs exceptionally well, with perfect precision and a very high recall.
- **For high-risk loans**, the model is strong, correctly identifying 94% of high-risk loans. While its precision (84%) is not perfect, it is still quite good, and the model's ability to recall high-risk loans is impressive.

### Justification for Recommendation:
The logistic regression model is highly recommended for use by the company due to its **high accuracy** and **excellent recall for high-risk loans**, which is crucial for identifying and managing risk. It correctly identifies nearly all high-risk loans, reducing the potential for missed defaults.

However, the company may want to explore further optimization techniques to improve the precision for high-risk loans, reducing false positives. But overall, this model is a robust solution for credit risk classification and should serve the company's needs effectively.

### Next Steps:
- Experiment with other classification algorithms to potentially improve precision for high-risk loans.
- Investigate strategies for handling class imbalance (as there are more healthy loans than high-risk loans in the dataset).
