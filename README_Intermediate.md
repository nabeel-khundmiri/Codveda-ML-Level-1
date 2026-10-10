# Telecom Customer Churn Prediction --- Intermediate Level

## Project Overview

This repository contains the Intermediate Level tasks completed as part
of the Codveda Technology Machine Learning Internship. It uses the IBM
Telco Customer Churn dataset to explore customer behavior and patterns
associated with churn.

Tasks covered: 1. **Logistic Regression** --- supervised classification
to predict customer churn. 2. **K-Means Clustering** --- unsupervised
learning to group customers with similar characteristics.

## Dataset

-   **Dataset:** IBM Telco Customer Churn
-   **Records:** 7,043 customers
-   **Target for Logistic Regression:** `Churn` (`Yes` / `No`)
-   **Excluded identifier:** `customerID`
-   **Preprocessing:** `TotalCharges` is converted to numeric. The 11
    blank values associated with zero-tenure customers are filled with
    `0`.

This is an educational analysis, not a production-ready churn system.

## Task 1: Logistic Regression

A Logistic Regression classifier is trained on preprocessed customer
features.

**Workflow** - Split data into training and test sets. - Impute missing
numeric and categorical values. - Standardize numeric features and
one-hot encode categorical features. - Train Logistic Regression. -
Evaluate accuracy, precision, recall, F1-score, and ROC-AUC. - Review
the confusion matrix and ROC curve. - Inspect coefficients and odds
ratios to understand feature associations.

**Interpretation note:** coefficients and odds ratios describe
associations in the fitted model; they do not establish causation.

## Task 2: K-Means Clustering

K-Means groups customers without using the `Churn` target as an input
feature.

**Workflow** - Transform customer features with the preprocessing
pipeline. - Use the elbow method to compare inertia across candidate
values of *K*. - Fit the selected K-Means model (the notebook uses
`K=4`). - Visualize clusters in two dimensions using PCA. - Profile
clusters using average tenure, monthly charges, and total charges. -
Compare churn distributions across clusters after clustering, for
interpretation only.

Cluster labels are arbitrary identifiers and do not automatically
represent churn-risk levels.

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
3.  Run the notebook cells in order, including preprocessing before
    model training.
4.  Review the metrics, plots, and exported CSV files.

The notebook may use a Google Drive path from the original Colab setup;
update it when running elsewhere.

## Expected Results Files

Expected intermediate-level exports include:

-   `logistic_regression_metrics.csv`
-   `intermediate_task3_kmeans_elbow.csv`
-   `intermediate_task3_customer_clusters.csv`
-   `intermediate_task3_cluster_profiles.csv`
-   `intermediate_task3_cluster_churn_distribution.csv`
-   `intermediate_task3_cluster_pca_coordinates.csv`

The exact files present depend on which notebook cells have run
successfully.

## Suggested Repository Structure

``` text
Codveda_ML_Level_2/
├── data/
│   └── raw/
│       └── Telco-Customer-Churn.csv
├── notebooks/
│   └── Telco_Customer_Churn_ML.ipynb
├── results/
└── README.md
```

## Limitations

-   Model performance depends on the dataset, split, and model settings.
-   Clustering is exploratory; clusters may not translate directly into
    actionable segments.
-   Further validation and monitoring would be required before business
    deployment.

## Internship Context

Prepared for the Intermediate Level of the Codveda Technology Machine
Learning Internship.
