# Machine-Learning

# Lab Report 01: Linear Regression on Diabetes Dataset

## Overview

This project applies Linear Regression to the Pima Indians Diabetes dataset to predict whether a person has diabetes (`Outcome = 1`) or not (`Outcome = 0`). The analysis includes data preprocessing, model training, and evaluation using common classification metrics.

## Dataset

The dataset used is `diabetes.csv`, containing the following features:

- Pregnancies
- Glucose
- BloodPressure
- SkinThickness
- Insulin
- BMI
- DiabetesPedigreeFunction
- Age
- Outcome (Target: 1 = diabetic, 0 = non-diabetic)

## Preprocessing Steps

1. Replace Zeros with Column Means:  
   For specific columns (`Glucose`, `BloodPressure`, `SkinThickness`, `Insulin`, `BMI`), all zero values (which are biologically implausible) are replaced with the mean of non-zero values.

2. Extreme Value Substitution:  
   - Set the glucose value of the first row to the maximum glucose in the dataset.
   - For rows with minimum age, their glucose is set to the minimum glucose value.

## Model Training

- Model: `LinearRegression` from scikit-learn.
- Train/Test Split: 80% training and 20% testing.
- Target: The model predicts a continuous value which is then rounded to 0 or 1 for binary classification.

## Evaluation Metrics

After rounding the predictions, the model is evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix

## Example Output

Confusion Matrix:
[[79 21]
[27 27]]
Accuracy: 0.688
Precision: 0.563
Recall: 0.500
F1-Score: 0.530



## Note

Linear Regression is not typically used for classification tasks. While it provides a rough baseline, more appropriate models (such as Logistic Regression or Decision Trees) are generally better suited for binary classification.
