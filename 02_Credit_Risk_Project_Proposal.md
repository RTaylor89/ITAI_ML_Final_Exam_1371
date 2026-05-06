# Credit Risk Midterm Project Proposal

## Objective
This project uses the Kaggle Credit Risk Dataset to prepare a real-world loan dataset for a machine learning exercise. The main goal is to clean the data, engineer useful features, and organize the results so the `loan_status` column can later be used for a binary classification model that predicts whether a borrower is likely to represent loan risk.

## Dataset Overview
The dataset contains borrower demographics, employment length, income, home ownership, loan purpose, loan grade, interest rate, previous default history, and credit history length. Early review shows missing values in fields such as `loan_int_rate` and `person_emp_length`, along with a few unrealistic values that need to be handled carefully.

## Planned Data Preparation
The raw file will be split into 70% training data and 30% testing data before any analysis. Exploratory data analysis will be performed only on the training split. The training data will then be cleaned by converting blanks to missing values, filling nulls with appropriate methods, handling unrealistic outliers, encoding categorical variables, applying one-hot encoding, creating new ratio-based features, normalizing skewed numeric fields, and scaling continuous values to a 0-to-1 range. The testing split will remain untouched in raw form.

## Expected Outcome
At the end of the project, the deliverables will include the untouched raw dataset, raw training and testing splits, a cleaned training dataset, a final clean dataset, and a Jupyter notebook that shows the data before and after preprocessing. The finished dataset will be ready for later machine learning models such as logistic regression, decision trees, random forests, or gradient boosting classifiers.
