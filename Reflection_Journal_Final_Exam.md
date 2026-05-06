# Credit Risk Midterm Reflection Journal

## Overview
This project focused on turning a raw credit risk dataset into a cleaner, model-ready dataset for a machine learning exercise. The Kaggle Credit Risk Dataset was used with `loan_status` treated as the target variable for a binary classification problem. One of the most important design decisions was separating the data into 70% training and 30% testing before preprocessing or analysis began. This ensured the testing data stayed isolated and untouched while all preprocessing work was performed strictly on the training dataset.

## What Was Completed
During exploratory data analysis on the training data, the dataset structure was reviewed using `head()`, `info()`, `describe()`, class distributions, and missing-value summaries. Missing values were identified in the interest rate and employment length columns, along with unrealistic values such as extremely large employment lengths.

To improve data quality:
- Blank values were converted into proper missing values
- `loan_int_rate` was imputed using grouped medians based on `loan_grade`
- `person_emp_length` values above 100 were capped instead of scaled
- Median imputation was applied where appropriate

Several engineered features were added to strengthen predictive capability:
- Debt-to-income ratio
- Income per credit year
- Credit-history-to-age ratio

Categorical features were encoded based on feature type:
- Binary encoding for prior defaults
- Ordinal encoding for `loan_grade`
- One-hot encoding for nominal features like home ownership and loan intent

Skewed financial variables such as:
- `person_income`
- `loan_amnt`

were normalized using transformations before scaling.

## Final Takeaway
The final preprocessing pipeline transformed the dataset from a raw financial dataset into a cleaner and repeatable machine learning workflow. The notebook now clearly demonstrates proper train/test separation, consistent preprocessing logic, and feature engineering practices suitable for future classification modeling.

This project reinforced how important preprocessing decisions are in machine learning workflows. Model performance depends heavily on clean data, meaningful features, and maintaining strict separation between training and testing datasets to avoid leakage and inflated evaluation results.
