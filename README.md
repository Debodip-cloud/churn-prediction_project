# churn-prediction_project
This project implements a customer churn prediction model using machine learning techniques. The goal is to predict the probability that a customer will churn based on historical behavioral and demographic data.
Overview

This project implements a customer churn prediction model using machine learning techniques. The goal is to predict the probability that a customer will churn based on historical behavioral and demographic data.

The model is built using Python and scikit-learn, with an optional XGBoost implementation for high performance.

The project includes:

Data preprocessing (handling missing values, encoding categorical variables, scaling numeric features)

Handling imbalanced datasets

Feature engineering for better predictive performance

Model training, validation, and ROC AUC evaluation

Generating predicted probabilities for test data

Dataset

The dataset contains customer information and a target column indicating churn:

CustomerID – unique identifier

Churn – target variable (1 = churn, 0 = no churn)

Multiple numerical and categorical features describing customer behavior and services

Replace train_df and test_df with your dataset CSV files.

Features

Automatic detection and preprocessing of numerical and categorical features

Missing value imputation using median for numeric and most frequent for categorical

Scaling of numerical features

One-hot encoding for categorical features

Optional feature engineering for service counts

Models

Random Forest – baseline model

XGBoost – high-performance boosting model for better ROC AUC

HistGradientBoostingClassifier – built-in scikit-learn boosting model (alternative to XGBoost if installation is not possible)

Usage

Clone the repository:

git clone https://github.com/yourusername/churn-prediction.git
cd churn-prediction

Install dependencies:

pip install -r requirements.txt

Or install xgboost separately if using that model:

pip install xgboost

Update the dataset paths in the notebook or script:

train_df = pd.read_csv("train.csv")
test_df = pd.read_csv("test.csv")

Run the script or notebook. The output will include:

Validation ROC AUC score

Predicted probabilities for test set

Evaluation

The primary evaluation metric is ROC AUC (Receiver Operating Characteristic – Area Under Curve).
Typical results:

Random Forest baseline: ~0.73–0.75

XGBoost / HistGradientBoosting: ~0.80–0.85

Files

churn_prediction.ipynb – Jupyter notebook with full preprocessing, model training, and prediction pipeline

requirements.txt – Python package dependencies

Author

Shuvam Kumar – Data Scientist | Fintech & ML enthusiast
