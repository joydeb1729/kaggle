# Titanic Survival Prediction Model

## Overview
This project aims to predict the survival of passengers on the Titanic using machine learning models. The solution includes steps in **Exploratory Data Analysis (EDA)**, **Feature Engineering (FE)**, and **Modeling**, with evaluation through cross-validation and hyperparameter tuning to optimize performance.

---

## 1. Exploratory Data Analysis (EDA)

### 1.1 Data Loading and Inspection
- The Titanic dataset was loaded and inspected for structure and data types.
- Key columns: `PassengerId`, `Name`, `Ticket`, `Survived`, `Pclass`, `Sex`, `Age`, `SibSp`, `Parch`, `Fare`, `Embarked`, and `Cabin`.

### 1.2 Handling Missing Data
- Missing values in `Age`, `Cabin`, and `Embarked` were handled:
  - `Age`: Filled with the median value or grouped into categories.
  - `Cabin`: Filled with the most frequent value within each `Pclass`.
  - `Embarked`: Filled with the most frequent value (`S`).
  
### 1.3 Categorical Data Encoding
- `Sex` and `Embarked` were encoded into numeric values.
- `Cabin` was encoded as a binary variable indicating the presence or absence of a cabin.

### 1.4 Visualizing Data
- Survival rates were visualized for various features like `Pclass`, `Sex`, and `Age` to uncover patterns and insights.

---

## 2. Feature Engineering (FE)

### 2.1 Creating New Features
- **Age Binning**: `Age` was categorized into bins (e.g., `Child`, `Young`, `Adult`, `Senior`) to help the model better understand the age groups.

### 2.2 Encoding Categorical Features
- `Sex` and `Embarked` were converted to numerical values using label encoding.

### 2.3 Feature Selection
- Irrelevant columns such as `PassengerId`, `Name`, and `Ticket` were dropped.

### 2.4 Correlation Analysis
- A heatmap was generated to assess correlations between numerical features. Unrelated features were considered for removal.

---

## 3. Modeling

### 3.1 Model Selection
The following models were tested:
- Logistic Regression
- Decision Tree Classifier
- K-Nearest Neighbors (KNN)
- Support Vector Classifier (SVC)
- Naive Bayes
- Random Forest Classifier

### 3.2 Cross-Validation
- Cross-validation (5-fold) was used to evaluate the models' accuracy.

### 3.3 Hyperparameter Tuning
- **Decision Tree Classifier** was optimized using **RandomizedSearchCV** for selecting the best hyperparameters.

### 3.4 Model Evaluation
- The **Decision Tree Classifier** achieved:
  - **Test Accuracy**: 86.84%
  - **Train Accuracy**: 86.76%
- Cross-validation showed an accuracy of **80.47%**, which improved after tuning.

---

## 4. Conclusion
- The **Decision Tree Classifier** was selected as the best model after optimization, with a high test accuracy of 86.84%.
- Cross-validation and hyperparameter tuning improved the model's performance.
- The same approach can be applied to other models to optimize performance.
