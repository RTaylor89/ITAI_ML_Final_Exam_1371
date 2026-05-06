# Credit Risk Final Machine Learning Project

This is an individual final project using the Kaggle Credit Risk Dataset.

The project builds a binary classification workflow to predict `loan_status`.

## Main Deliverables

- `09_Credit_Risk_Final_Modeling_Notebook.ipynb`  
  Main modeling notebook with verbose comments and presentation-ready explanations.

- `10_Model_Comparison_Table.pdf`  
  PDF table summarizing model performance.

- `11_Final_Project_Report.pdf`  
  Final written report.

- `13_Credit_Risk_Presentation.pptx`  
  Short presentation deck.

- `14_Presentation_Speaker_Notes.md`  
  Speaker notes for walking through the project.

## Split Strategy

The final modeling workflow uses a 70% / 15% / 15% split:

- 70% Training Data: used to train the models.
- 15% Validation Data: used for model comparison and ensemble selection.
- 15% Testing Data: isolated until final evaluation.

The easiest way to explain the split is that the original 30% holdout was divided into two equal parts:
15% validation and 15% final test.

## Key Preprocessing Corrections

- `person_emp_length` is capped at 100 instead of scaled.
- `loan_grade` is ordinal encoded as A=1 through G=7.
- `person_income` and `loan_amnt` are log-transformed to address skew.
- Validation and test preprocessing reuse values learned from training data only.

## Models Trained

- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier
- Gradient Boosting Classifier
- K-Nearest Neighbors Classifier
- Support Vector Classifier
- Voting Ensemble
- Bayesian-style Weighted Ensemble
