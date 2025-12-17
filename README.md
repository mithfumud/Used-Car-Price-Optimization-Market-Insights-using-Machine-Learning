# Used Car Price Prediction (CarDekho Dataset)

This project aims to build a machine learning model that can predict the selling price of a used car based on its features. The main goal of the project was to understand and practice the complete machine learning pipeline on real-world tabular data, rather than only optimizing for accuracy.

---

## Dataset

The dataset is taken from CarDekho and contains information about used cars such as:
- Year of manufacture
- Kilometers driven
- Fuel type
- Transmission type
- Ownership history
- Selling price (target variable)

---

## Problem Statement

Used car prices vary widely and are influenced by multiple numerical and categorical features. The dataset also contains skewed price distributions and potential outliers.  
The objective of this project is to build a regression model that can predict car prices accurately while properly handling categorical variables, skewness, and outliers.

---

## Approach

### Data Preprocessing
- Checked for missing values (none were present).
- Encoded categorical variables:
  - One-Hot Encoding for non-ordinal categorical features.
  - Label Encoding for features with an inherent order.
- Created a new feature:

car_age = 2025 - year

since car age represents depreciation better than the raw year.
- Removed extreme outliers in selling price using the IQR method.

---

### Exploratory Data Analysis (EDA)
- Observed that the selling price distribution is right-skewed, with most cars priced under ₹5 lakhs.
- Used boxplots, bar charts, and correlation heatmaps to understand feature relationships.
- Found that car age, kilometers driven, and fuel type have a strong influence on selling price.

---

### Modeling
- Split the dataset into training and testing sets.
- Trained and compared multiple regression models:
- Random Forest Regressor
- XGBoost Regressor
- CatBoost Regressor
- Evaluated models using R² score and RMSE.
- Analyzed feature importance from tree-based models.

---

## Results

- CatBoost performed the best among all models, achieving an R² score of around 85%.
- Car age, kilometers driven, and fuel type were identified as the most important predictors.
- Model performance improved after feature engineering and removing outliers.
- The final pipeline covered data cleaning, feature engineering, EDA, model training, evaluation, and comparison.

---

## Why CatBoost

CatBoost gave better performance mainly because of how it handles categorical variables. It uses ordered target encoding, which helps reduce data leakage and captures the effect of categories more effectively.  
Its ordered boosting technique also helps prevent overfitting, especially on small to medium-sized datasets.

---

## Key Learnings
- Feature engineering can have a significant impact on model performance.
- Handling outliers improves model stability.
- Tree-based models work well for non-linear relationships in tabular data.
- Model choice should be based on data characteristics, not just popularity.

---

## Tools and Libraries
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- XGBoost
- CatBoost

---

## Future Work
- Hyperparameter tuning using GridSearchCV or Optuna
- Applying log transformation to reduce price skewness
- Deploying the model using Flask or FastAPI

---

## Motivation

I built this project to get hands-on experience with the full machine learning workflow and to understand how 
