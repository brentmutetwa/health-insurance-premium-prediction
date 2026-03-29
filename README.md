# Health Insurance Premium Prediction Model

A machine learning model that predicts individual health insurance premiums using the [US Health Insurance dataset](https://www.kaggle.com/datasets/teertha/ushealthinsurancedataset). Built in Python using **scikit-learn**, this project demonstrates a full regression workflow from exploratory data analysis to model deployment.
[View the code here](https://colab.research.google.com/drive/1q_T3E1scqp47RYt_w-rE-yY3HODi5gNZ?usp=sharing).
## Overview

This project focuses on predicting medical insurance charges based on demographic and health-related features. The goal is to support **risk-based pricing** and improve how insurers estimate expected healthcare costs.

Key Capabilities:

* Predicts insurance premiums (continuous values)
* Captures non-linear relationships in healthcare costs
* Identifies key drivers of insurance pricing
* Provides an interactive interface for real-time predictions

## Dataset

Dataset from Kaggle: [US Health Insurance Dataset](https://www.kaggle.com/datasets/teertha/ushealthinsurancedataset).
The dataset contains **1,338 observations** with 6 features:

* "age": Age of the individual
* "sex": Gender (male/female)
* "bmi": Body Mass Index
* "children": Number of dependents
* "smoker": Smoking status (yes/no)
* "region": Residential region (northeast, northwest, southeast, southwest)
* "charges": (Target variable) Medical insurance cost

## Project Workflow

### 1. Data Import & Exploration

Loaded dataset and validated structure.
No missing values detected.
Analyzed feature distributions and target skewness.

### 2. Data Preprocessing

* Binary encoding for "sex" and "smoker"
* One-hot encoding for "region" to avoid false ordinal relationships
* No imputation required

### 3. Exploratory Data Analysis

* Identified strong right-skew in "charges"
* Explored correlations and feature relationships
* Observed clear non-linear patterns

### 4. Model Development

* Built baseline “dumb” model for benchmarking
* Trained **Random Forest Regressor**
* Chosen due to ability to handle non-linearity and skewed data

### 5. Evaluation

Metrics used:

* RMSE (Root Mean Squared Error)
* MAE (Mean Absolute Error)

Baseline vs Model:

* Significant reduction in both RMSE and MAE
* Model handled non-linear cost drivers effectively

### 6. Hyperparameter Tuning

Optimized using key parameters:

* max_depth = 5
* min_samples_leaf = 6
* n_estimators = 6

Performance improvement:

* RMSE reduced from 4734.21 → 4433.41
* MAE reduced from 2758.25 → 2543.88

### 7. Deployment

* Model saved using joblib
* Interactive interface built with **ipywidgets**
* Allows dynamic premium prediction based on user inputs

## Key Insights

* **Smoking status dominates pricing** → strongest predictor by far
* **BMI and age matter** → moderate but consistent impact
* **Non-linearity is critical** → linear models would underperform
* **Regional effects are weak** → minimal predictive contribution

## Limitations

* Small dataset (1,338 records) limits generalization
* No external validation dataset used
* Limited feature set (no medical history, income, etc.)
* Random Forest not fully optimized (very low n_estimators = underfit risk)

## 👤 Author

**Brenton Mutetwa**

[GitHub: github.com/brentmutetwa](github.com/brentmutetwa)

[LinkedIn: linkedin.com/in/brenton-mutetwa-95470b253](linkedin.com/in/brenton-mutetwa-95470b253)

Email: [mutetwabrentont@gmail.com](mailto:mutetwabrentont@gmail.com)
