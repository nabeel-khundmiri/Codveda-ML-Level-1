# Telecom Customer Churn Prediction --- Advanced Level

## Project Overview

This repository contains the Advanced Level tasks completed as part of
the Codveda Technology Machine Learning Internship. It uses the IBM
Telco Customer Churn dataset to build and evaluate classification models
for identifying customers who may churn.

Tasks covered: 1. **Random Forest** --- ensemble classification with
randomized hyperparameter search and feature-importance analysis. 2.
**Support Vector Machine (SVM)** --- classification using linear and RBF
kernels.

## Dataset

-   **Dataset:** IBM Telco Customer Churn
-   **Records:** 7,043 customers
-   **Target:** `Churn` (`Yes` / `No`)
-   **Excluded identifier:** `customerID`
-   **Preprocessing:** `TotalCharges` is converted to numeric and blank
    values are filled with `0`. Numeric features are imputed and scaled;
    categorical features are imputed and one-hot encoded.

This is an educational project using historical customer records, not a
deployed production system.

## Task 1: Random Forest Classifier

A Random Forest model is trained to predict customer churn.
Hyperparameters are explored using `RandomizedSearchCV` with stratified
cross-validation.

**Workflow** - Reuse the preprocessing pipeline for numeric and
categorical features. - Train a Random Forest classifier. - Search a
limited set of hyperparameter combinations using cross-validation. -
Evaluate the selected model using accuracy, precision, recall, F1-score,
and ROC-AUC. - Review the classification report and confusion matrix. -
Rank input features using the model's feature-importance scores.

The search explores a subset of parameter combinations to keep runtime
manageable. Feature importance does not prove that a feature causes
churn.

## Task 2: Support Vector Machine (SVM)

Two SVM variants are compared: - **Linear SVM** - **RBF-kernel SVM**

**Workflow** - Train both SVM variants on the processed training data. -
Evaluate accuracy, precision, recall, F1-score, and ROC-AUC. - Review
the RBF SVM classification report and confusion matrix. - Plot ROC
curves to compare model discrimination.

Select a model based on the evaluation results and the business
objective, not accuracy alone. For churn detection, precision and recall
for the `Yes` class are particularly useful.

## Tools and Libraries

-   Python, pandas, NumPy
-   scikit-learn
-   Matplotlib and Seaborn
-   Google Colab / Jupyter Notebook

## How to Run

1.  Open `Telco_Customer_Churn_ML.ipynb` in Google Colab or Jupyter
    Notebook.
2.  Put `Telco-Customer-Churn.csv` in the expected data directory, or
    update the notebook's file path.
3.  Run the data-loading and preprocessing cells first.
4.  Run the Random Forest and SVM sections in order.
5.  Review the metrics, plots, and exported CSV files.

The notebook may use a Google Drive path from the original Colab setup;
update it when running elsewhere.

## Expected Results Files

Expected advanced-level exports include:

-   `random_forest_metrics.csv`
-   `random_forest_feature_importance.csv`
-   `random_forest_best_parameters.csv`
-   `advanced_task2_svm_metrics.csv`

The exact files present depend on which notebook cells have run
successfully.

## Suggested Repository Structure

``` text
Codveda_ML_Level_3/
├── data/
│   └── raw/
│       └── Telco-Customer-Churn.csv
├── notebooks/
│   └── Telco_Customer_Churn_ML.ipynb
├── results/
└── README.md
```

## Limitations

-   The hyperparameter search is limited and may not find the globally
    optimal configuration.
-   Metrics depend on the data split, preprocessing, and model settings.
-   Performance on historical data may differ from performance on future
    customers.
-   Deployment would require further validation, threshold selection,
    privacy/security controls, and ongoing monitoring.

## Internship Context

Prepared for the Advanced Level of the Codveda Technology Machine
Learning Internship.
