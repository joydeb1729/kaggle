# House Prices Prediction Project

This repository contains a comprehensive workflow for predicting house prices using machine learning models. The project is divided into three main stages, each documented in its respective Jupyter notebook:

## Notebooks Overview

### 1. Elementary Data Analysis of Housing Prices
- Conducts basic exploratory data analysis to understand the dataset.
- Includes statistical summaries, visualizations, and feature relationships.

### 2. Feature Engineering of Housing Prices
- Prepares the dataset for modeling through feature transformations.
- Handles missing values, encodes categorical variables, addresses skewness, and scales numerical features.
- Generates new features to enhance model performance.
- Outputs feature-engineered datasets: `train_x.csv`, `test_x.csv`, and `log_train_y.csv`.

### 3. Modeling for Housing Prices Prediction
- Implements machine learning models for price prediction.
- Compares multiple regression models (CatBoost, XGBoost, LightGBM, Gradient Boosting) using cross-validation.
- Applies an ensemble approach to generate final predictions.
- Produces the submission file for the competition.

## Repository Structure
```bash
/House-Prices-Prediction/
│
├── notebooks/
│   ├── 1_Elementary_Data_Analysis.ipynb
│   ├── 2_Feature_Engineering.ipynb
│   ├── 3_Modeling.ipynb
│
├── data/
│   ├── train.csv
│   ├── test.csv
│   ├── submission.csv
│   ├── train_x.csv
│   ├── test_x.csv
│   ├── log_train_y.csv
│
├── README.md
└── requirements.txt
