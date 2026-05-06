# Credit Risk Final Project — Speaker Notes

## Slide 1 — Project Overview

This project predicts loan default risk using the Kaggle Credit Risk Dataset.

The target variable is `loan_status`, so this is a binary classification problem.

The full workflow includes:
- data cleaning
- feature engineering
- model training
- validation comparison
- final test evaluation
- ensemble modeling

## Slide 2 — Preprocessing Corrections

The main preprocessing corrections were:

1. `person_emp_length` was capped at 100.
   - The raw dataset had a 123-year employment value.
   - That value is unrealistic, so it was capped instead of scaled.

2. `loan_grade` was ordinal encoded.
   - A=1, B=2, C=3, D=4, E=5, F=6, G=7.
   - This preserves the risk ordering of the grade.

3. Skew was addressed for:
   - `person_income`
   - `loan_amnt`

These were log-transformed so the model was not distorted by extreme financial values.

## Slide 3 — Data Split Strategy

The final split is 70% training, 15% validation, and 15% testing.

The simple explanation:

- 70% is used for training.
- The remaining 30% is held out.
- That 30% holdout is split evenly:
  - 15% validation
  - 15% final test

Validation is used to compare models.
Testing is saved for final evaluation only.

## Slide 4 — Modeling and Results

The notebook trains the required classification models:
- Logistic Regression
- Decision Tree
- Random Forest
- Gradient Boosting
- KNN
- Support Vector Classifier

It also compares:
- Voting Ensemble
- Bayesian-style Weighted Ensemble

The main takeaway is that tree-based and ensemble models generally perform better on this dataset because they handle nonlinear relationships better than simple linear models.
