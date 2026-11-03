# Predicting Hospital Readmissions Using Machine Learning

A comprehensive machine learning project designed to predict hospital readmissions using the FY 2025 Hospital Readmissions Reduction Program (HRRP) dataset. This repository evaluates and compares multiple supervised machine learning models--Decision Tree, Random Forest, and Gradient Boosting--to predict the Excess Readmission Ratio for hospitals across various clinical measures.

---

## Project Overview

Hospital readmissions are a critical benchmark for healthcare quality, efficiency, and cost management. This project analyzes national hospital performance data through multiple algorithms to determine which model achieves the highest predictive accuracy for excess readmission rates based on facility discharges, expected readmission rates, and clinical categories.

---

## Dataset Features

The dataset (`FY_2025_Hospital_Readmissions_Reduction_Program_Hospital.csv`) contains facility-level performance details, including:
* **Facility Identification:** Facility Name, Facility ID, State
* **Clinical Measures:** Measure Name (e.g., AMI, CABG, Heart Failure, Hip/Knee, Pneumonia)
* **Performance Metrics:** Number of Discharges, Number of Readmissions, Predicted Readmission Rate, Expected Readmission Rate, and Excess Readmission Ratio (Target Variable).

---

## Tech Stack & Libraries

* **Python** (3.x)
* **Pandas & NumPy** (Data manipulation and preprocessing)
* **Scikit-Learn** (Model training, evaluation, pipeline construction)
* **Matplotlib & Seaborn** (Data visualization and model performance plotting)

---

## Data Preprocessing & Pipeline

1. **Target Filtering:** Rows with missing values in the target variable (`Excess Readmission Ratio`) are dropped to ensure clean supervision labels.
2. **Feature Engineering & Selection:** Irrelevant or identifying metadata columns (`Facility Name`, `Facility ID`, `Start Date`, `End Date`) are removed.
3. **Categorical Encoding:** Categorical features such as `State` and `Measure Name` are mapped to numeric codes.
4. **Data Type Conversion:** Object columns and readmission numbers are safely coerced into numeric types.
5. **Train-Test Split:** The dataset is split into training and testing sets with an 80/20 ratio (`test_size=0.2`).

---

## Model Comparison Framework

The repository implements and compares **three different machine learning models** to evaluate regression performance:

1. **Decision Tree Regressor** 
2. **Random Forest Regressor** 
3. **Gradient Boosting Regressor** 

### Comparative Evaluation Metrics:
* **MAE:** Mean Absolute Error
* **MSE:** Mean Squared Error
* **RMSE:** Root Mean Squared Error
* **R2 Score:** Coefficient of Determination

---
