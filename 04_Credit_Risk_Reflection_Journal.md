# Credit Risk Midterm Reflection Journal

## Overview
This project focused on turning a raw credit risk dataset into a cleaner, model-ready dataset for a machine learning exercise. Our group used the Kaggle Credit Risk Dataset and treated `loan_status` as the target variable for a binary classification problem. One of the most important decisions we made was splitting the data into 70% training and 30% testing before any exploratory analysis or preprocessing. This kept the testing dataset isolated and untouched while all cleaning work was performed only on the training split.

## What We Accomplished
During exploratory data analysis on the training data, we reviewed the dataset structure with `head()`, `info()`, `describe()`, class counts, and missing-value summaries. We found missing values in the interest rate and employment length columns, and we also identified a few unrealistic values such as unusually high ages or employment lengths. To improve data quality, we converted blank values to proper missing values, used group-based imputation for `loan_int_rate` based on `loan_grade`, and used median imputation for `person_emp_length`. We also handled unrealistic training values before moving into the transformation stage.

For feature engineering, we created new variables such as debt-to-income ratio, income per credit year, and credit-history-to-age ratio. These features give the future model stronger signals than raw columns alone. We also encoded categorical information in multiple ways: binary encoding for previous default status, ordinal encoding for loan grade, and one-hot encoding for nominal variables like home ownership, loan intent, and age group. To complete the preprocessing pipeline, we normalized skewed numeric features with a Yeo-Johnson transformation and then scaled them with MinMaxScaler so they fall within a comparable range.

## Team Contributions
**Roderick Taylor** helped interpret the assignment requirements, enforce the rule that the testing data must remain untouched, and organize the final submission package so it works cleanly as a GitHub repository and class submission set.

**Lynnia Salter** contributed to exploratory data analysis and data quality review. She helped inspect the dataset structure, identify missing values, and confirm which columns needed special cleanup attention.

**Elijah Ghaya** contributed to the preprocessing design by helping shape the imputation, encoding, and feature engineering strategy. His input helped make the notebook more consistent with the team’s classroom style and workflow.

**Michael Rodriguez** contributed to the machine learning framing and documentation review. He helped connect the cleaned dataset to the future classification problem and reviewed the final narrative for the proposal, notebook, and reflection materials.

## Final Takeaway
As a team, we moved the dataset from a raw state to a refined and repeatable preprocessing pipeline. The final notebook now shows a clear before-and-after view of the training data, preserves the testing split exactly as required, and prepares the cleaned training data for future classification modeling. This project reinforced that good machine learning results depend heavily on careful data preparation, thoughtful feature engineering, and academically sound separation between training and testing data.
