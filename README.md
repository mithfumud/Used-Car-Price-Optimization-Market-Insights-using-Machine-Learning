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

