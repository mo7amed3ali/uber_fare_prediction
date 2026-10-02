# Uber Fare Prediction — Machine Learning Task 2

## Project Overview

This project focuses on preparing an Uber fare dataset for regression modeling and building a machine learning pipeline to predict fare amounts.

The project covers data preprocessing, feature encoding, feature scaling, outlier detection, cross-validation, and hyperparameter tuning.

## Dataset

- **Rows:** 487,742
- **Columns:** 26
- **Target Variable:** `fare_amount`
- **Problem Type:** Regression

## Data Preprocessing

The following steps were performed:

- Missing value analysis
- Duplicate detection
- Categorical feature encoding
- Numerical feature scaling
- Feature selection
- Outlier detection
- Train/Test splitting
- Cross-validation
- Hyperparameter tuning

### Data Quality

- Missing values: **0**
- Duplicate rows: **0**
- Detected outliers: **33,702 (8.64%)**

The detected outliers were identified but not automatically removed because some high fare values may represent valid trips.

## Models

### Baseline Model

**Linear Regression**

### Tuned Model

**Random Forest Regressor**

Hyperparameters were optimized using `RandomizedSearchCV` with 5-fold cross-validation.

## Model Results

| Model | MAE | RMSE | R² |
|---|---:|---:|---:|
| Linear Regression | 2.4143 | 4.8874 | 0.7368 |
| Tuned Random Forest | 1.6465 | 3.4732 | 0.8671 |

## Best Random Forest Parameters

```text
n_estimators = 73
max_depth = 20
max_features = 0.7
min_samples_split = 5
min_samples_leaf = 5
