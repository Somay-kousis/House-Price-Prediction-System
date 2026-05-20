# House Price Prediction System

<div align="center">

![Python](https://img.shields.io/badge/Python-3.9-blue?style=for-the-badge\&logo=python)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-orange?style=for-the-badge\&logo=scikitlearn)
![XGBoost](https://img.shields.io/badge/XGBoost-Gradient%20Boosting-red?style=for-the-badge)
![CatBoost](https://img.shields.io/badge/CatBoost-Boosting-yellow?style=for-the-badge)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-black?style=for-the-badge\&logo=pandas)
![NumPy](https://img.shields.io/badge/NumPy-Numerical-blue?style=for-the-badge\&logo=numpy)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-green?style=for-the-badge)
![Seaborn](https://img.shields.io/badge/Seaborn-EDA-teal?style=for-the-badge)
![Kaggle](https://img.shields.io/badge/Kaggle-House%20Prices-20BEFF?style=for-the-badge\&logo=kaggle)

</div>

---

## Overview

An end-to-end machine learning pipeline built on the Kaggle House Prices dataset using advanced preprocessing, feature engineering, boosting models, and cross-validation techniques.

This project focuses heavily on:

* feature engineering
* preprocessing pipelines
* handling missing values
* model comparison
* boosting methods
* evaluation metrics
* hyperparameter tuning

The project evolved from a simple linear regression baseline into a fully engineered boosting-based regression system.

---

## Problem Statement

Predict residential house prices based on various structural, quality, neighborhood, and property-related features.

Dataset contains:

* numerical features
* categorical features
* ordinal quality features
* missing values
* skewed distributions
* outliers

---

## Tech Stack

| Category            | Tools                                |
| ------------------- | ------------------------------------ |
| Language            | Python                               |
| Data Processing     | Pandas, NumPy                        |
| Visualization       | Matplotlib, Seaborn                  |
| ML Framework        | scikit-learn                         |
| Boosting Models     | XGBoost, CatBoost                    |
| Model Evaluation    | Cross Validation, RMSE, R²           |
| Feature Engineering | Custom engineered features           |
| Pipeline System     | sklearn Pipeline + ColumnTransformer |

---

## Exploratory Data Analysis

Performed extensive EDA on:

* feature distributions
* skewness
* correlations
* categorical impacts
* neighborhood pricing patterns
* quality-based pricing trends
* outlier detection

### Visualizations Used

* histograms
* KDE plots
* scatter plots
* box plots
* bar plots
* correlation analysis

---

## Feature Engineering

Created advanced engineered features including:

| Feature           | Purpose                    |
| ----------------- | -------------------------- |
| GarageAge         | Garage recency             |
| HouseAge          | House modernization        |
| ConstructionScore | Combined room + bath score |
| TotalPorchSF      | Outdoor area aggregation   |
| TotalSF           | Total living space         |
| TotalQuality      | Combined quality score     |
| GarageScore       | Garage utility metric      |
| FinishedBsmtRatio | Basement usability         |
| OutdoorScore      | Outdoor utility score      |
| HasGarage         | Binary utility feature     |
| HasPool           | Binary utility feature     |
| HasBasement       | Binary utility feature     |
| Has2ndFloor       | Binary utility feature     |
| HasFireplace      | Binary utility feature     |
| HasPorch          | Binary utility feature     |
| HasMasonry        | Binary utility feature     |

---

## Missing Value Handling

Applied different strategies based on feature semantics:

### Numerical Features

* median imputation
* zero-imputation where absence carried meaning

### Categorical Features

* `"NA"` category creation
* semantic missing handling

### Domain-Specific Handling

* basement-related features
* garage-related features
* masonry features
* fence and miscellaneous features

---

## Preprocessing Architecture

Built modular preprocessing pipelines using:

* `Pipeline`
* `ColumnTransformer`
* `FunctionTransformer`
* `OrdinalEncoder`
* `OneHotEncoder`
* `StandardScaler`

### Separate Pipelines

* log transformed numerical features
* ordinal quality features
* categorical one-hot encoded features
* basement exposure ordinal pipeline

---

## Models Used

### Linear Regression

Initial baseline model.

### Ridge-style Regularization Concepts

Explored regularization intuition and overfitting control.

### XGBoost

Implemented gradient boosting with hyperparameter tuning.

### CatBoost

Final optimized boosting model with:

* categorical-aware boosting
* regularization
* tuned depth
* learning rate optimization

---

## Hyperparameter Tuning

Used:

* `RandomizedSearchCV`
* cross-validation
* parameter search spaces

### Tuned Parameters

* iterations
* learning_rate
* depth
* l2_leaf_reg
* bagging_temperature
* random_strength
* max_depth
* subsample
* regularization parameters

---

## Evaluation Metrics

Regression metrics used:

* R² Score
* MAE
* RMSE
* Cross Validation RMSE

### Additional Analysis

* worst prediction inspection
* error analysis dataframe
* prediction comparison tables

---

## Key Learning Outcomes

This project involved practical understanding of:

* preprocessing pipelines
* feature engineering
* data leakage
* train/test workflow
* boosting algorithms
* hyperparameter tuning
* regression metrics
* model evaluation
* handling skewed data
* categorical encoding
* outlier handling
* cross validation

---

## Project Structure

```bash
House-Price-Prediction-System/
│
├── train.csv
├── test.csv
├── notebook.ipynb
├── submission.csv
├── README.md
│
├── preprocessing/
├── feature_engineering/
├── models/
└── evaluation/
```

---

## Results

| Model             | Performance      |
| ----------------- | ---------------- |
| Linear Regression | Baseline         |
| XGBoost           | Improved         |
| CatBoost          | Best Performance |

Final Kaggle score reached approximately:

```text
0.90
```

---

## Future Improvements

* custom sklearn transformers
* SHAP explainability
* stacking ensembles
* Optuna hyperparameter tuning
* deployment pipeline
* model serving API
* experiment tracking

---

## Author

Built as part of a practical ML learning journey focused on:

* understanding model behavior
* engineering features
* building reproducible pipelines
* and learning real-world machine learning workflows.
