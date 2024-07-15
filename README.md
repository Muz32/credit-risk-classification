# credit-risk-classification

## Overview of the Analysis
The purpose of this analysis is to predict the creditworthiness of borrowers using a logistic regression machine learning model. Historical lending data was used to build, train, and test the model. The lending data includes the following features:
- **loan_size**: The amount of the loan given to the borrower.
- **interest_rate**: The percentage of interest charged on the loan.
- **borrower_income**: The annual income of the borrower.
- **debt_to_income**: The ratio of the borrower’s total debt to their income, calculated as total debt divided by borrower income.
- **num_of_accounts**: The number of credit accounts or loans the borrower has.
- **derogatory_marks**: Negative marks on a credit report, such as late payments or defaults.
- **total_debt**: The total amount of debt the borrower has across all accounts.
- **loan_status**: This indicates whether the loan is healthy (0) or has a high risk of defaulting (1).

In the model, the target variable was ‘loan_status’ (the variable the model aimed to predict), while the rest of the features served as input variables to provide the information needed to predict the target. The model was built using the following steps:
1. **Loading** the lending data into a pandas DataFrame.
2. **Separating** the input variables (X) from the target variable (y). The input variables were stored in a new DataFrame, while the target variable was stored in an array.
3. **Splitting** the X and y data into training and testing datasets.
4. **Fitting** a logistic regression model to the training data.
5. **Evaluating** the model’s performance by making predictions and using a confusion matrix and classification report to assess the model’s performance.

## Results

### Classification Report
Key insights from the classification report include the precision and recall scores for each class of predicted variables, as well as the overall accuracy and weighted average scores of the analysis. The following are the key insights:

#### Class 0 (Healthy Loan):
- **Precision: 1.00** - Of all the loans predicted to be healthy, 100% were actually healthy.
- **Recall: 0.99** - Of all the healthy loans, 99% were correctly identified.

#### Class 1 (High-Risk Loan):
- **Precision: 0.85** - Of all the loans predicted to be high-risk, 85% were actually high-risk.
- **Recall: 0.91** - Of all the high-risk loans, 91% were correctly identified.

### Overall Performance Metrics:
- **Accuracy: 0.99** - The overall accuracy of the model, indicating that 99% of all predictions were correct.
- **Weighted Average**:
  - **Precision: 0.99** - Precision weighted by the number of true instances for each class/label.
  - **Recall: 0.99** - Recall weighted by the number of true instances for each class/label.

### Confusion Matrix
The confusion matrix provides the following information:
- **True Negatives (TN): 18,663** - These are healthy loans correctly predicted as healthy.
- **False Positives (FP): 102** - These are healthy loans incorrectly predicted as high-risk.
- **False Negatives (FN): 56** - These are high-risk loans incorrectly predicted as healthy.
- **True Positives (TP): 563** - These are high-risk loans correctly predicted as high-risk.

## Summary
The overall **accuracy** of the model is immensely high at a score of 0.99. This signifies that the model correctly classifies almost all of the loans.

When looking at the individual class scores for identifying **healthy loans**, the model performs excellently, with precision and recall scores both close to 1.00.

For identifying **high-risk loans**, the model also performs well, with a good precision of 0.85 and a recall of 0.91.However, there is still scope for further refinement, especially in reducing the false positives (102) and false negatives (56).

The **weighted average** metrics are close to 1.00, suggesting that the **model handles the imbalance between classes well**, given that there are many more healthy loans than high-risk loans.

In light of the above, it is deduced that the model performs exceptionally well in predicting the creditworthiness of new borrowers.  **It is recommended that the trained logistic regression model be used to help in ascertaining whether loans to new borrowers should be approved or rejected.**

## Source of Data
The dataset was provided by edX Boot Camps LLC.

## Folder Structure
```
credit-risk-classification (Root Folder)
└── Credit_Risk/
    ├── credit_risk_classification.ipynb - Jupyter notebook containing the machine learning model and analysis
    └── Resources/
        └── lending_data.csv - CSV file with source data for machine learning model.
```
