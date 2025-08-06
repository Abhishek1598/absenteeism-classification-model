# 📊 Employee Absenteeism Analysis & Prediction

This project focuses on analyzing patterns in employee absenteeism and building a logistic regression model to predict excessive absenteeism.

---

## 🚀 Project Overview

- Dataset: [UCI Absenteeism at Work](https://archive.ics.uci.edu/ml/datasets/Absenteeism+at+work)
- Algorithm: Logistic Regression
- Objective: Predict whether an employee is likely to be excessively absent based on historical attributes.

---

## 🛠️ Features & Pipeline

- ✅ Data Cleaning & Feature Engineering
- ✅ Exploratory Data Analysis (EDA)
- ✅ Target Label Creation
- ✅ Logistic Regression Modeling
- ✅ Deployment with Pickle
- ✅ Custom Python Module for Predictions

---

## 📁 Files Included

| File | Description |
|------|-------------|
| `Project_Absenteeism.ipynb` | Full EDA, modeling, and evaluation notebook |
| `absenteeism_module.py` | Python class for deploying the model |
| `model` / `scaler` | Serialized model and scaler |
| `Absenteeism_predictions.csv` | Sample prediction output |
| `final_summary_markdown.md` | Summary of entire project |
| `requirements.txt` | Dependencies for the project |

---

## 🔮 Sample Prediction Code

```python
from absenteeism_module import absenteeism_model

model = absenteeism_model('model', 'scaler')
model.load_and_clean_data('new_data.csv')
results = model.predicted_outputs()
results.to_csv('Absenteeism_predictions.csv', index=False)

