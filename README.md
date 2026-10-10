Telecom Customer Churn Prediction Using Machine Learning
Project Overview
This project uses the IBM Telco Customer Churn dataset to explore customer churn prediction using machine learning. The objective is to identify customers who may leave a telecom service provider and evaluate classification models that could support customer-retention decisions.
Dataset
Dataset: IBM Telco Customer Churn
Rows: 7,043 customers
Original columns: 21
Target: Churn (Yes or No)
Identifier removed from features: customerID
The dataset describes a fictional telecom provider. Results are experimental and should not be interpreted as a deployed or real-time prediction service.
Project Tasks
Basic Level — Task 1: Data Preprocessing
Inspected dataset structure and data quality.
Converted TotalCharges to numeric format.
Handled blank TotalCharges entries associated with zero tenure using a documented zero-value assumption.
Split the data into training and testing sets.
Used median imputation and standard scaling for numerical features.
Used most-frequent imputation and one-hot encoding for categorical features.
Used a preprocessing pipeline to keep training and test transformations consistent.
Basic Level — Task 3: K-Nearest Neighbors (KNN)
Trained a KNN classifier to predict customer churn.
Evaluated accuracy, precision, recall, F1-score, and the confusion matrix.
Compared multiple values of K.
Intermediate Level — Task 1: Logistic Regression
Trained a binary classification model.
Evaluated classification metrics and ROC-AUC.
Plotted the ROC curve.
Examined model coefficients and odds ratios.
Advanced Level — Task 3: Random Forest
Trained a Random Forest classifier.
Searched a selection of hyperparameter combinations using stratified cross-validation.
Evaluated test-set performance.
Examined feature importance.
Tools and Libraries
Python
pandas and NumPy
scikit-learn
Matplotlib
Seaborn
Google Colab and Google Drive
Project Structure
Codveda_ML_Level_1/
├── data/
│   └── raw/
│       └── Telco-Customer-Churn.csv
├── notebooks/
│   └── Telco_Customer_Churn_KNN.ipynb
├── results/
│   ├── basic_task1_preprocessing_summary.csv
│   ├── basic_task3_knn_k_comparison.csv
│   ├── basic_task3_knn_baseline_metrics.csv
│   ├── basic_task3_knn_confusion_matrix.csv
│   ├── logistic_regression_metrics.csv
│   ├── random_forest_metrics.csv
│   ├── random_forest_feature_importance.csv
│   └── random_forest_best_parameters.csv
└── README.md

The results directory may contain additional outputs generated during experimentation.
How to Run
Open the notebook in Google Colab.
Ensure the dataset is available at the expected Google Drive path.
Mount Google Drive.
Run the notebook cells in order.
Review the evaluation metrics and visualizations in the notebook.
Check the results/ directory for exported CSV files.
Evaluation and Limitations
Accuracy alone does not fully describe churn-model performance. Precision and recall for the churn-positive class are also important because missed churners and unnecessary retention interventions have different business costs.
The dataset is historical, and model performance may change on new customer populations. Feature importance and model coefficients indicate patterns learned from the data; they do not establish causation.
Internship
Prepared as part of the Codveda Technology Machine Learning Internship.
