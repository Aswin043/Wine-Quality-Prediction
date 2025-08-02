# 🍷 Wine Quality Prediction with MLflow & Machine Learning 🤖

This project aims to predict the quality of wine based on its physicochemical properties using supervised machine learning models. It features end-to-end experimentation tracking and reproducibility using MLflow.

---

## 📌 Project Overview

Wine quality is influenced by multiple chemical components such as acidity, sugar content, and pH. In this project, we build predictive models to classify wine quality on a scale (typically 0–10), using a dataset of red and white wine samples.

Key objectives:
- Build and evaluate regression/classification models
- Track experiments using MLflow
- Log metrics, parameters, and artifacts
- Select and register the best model for deployment

---

## 🧪 Dataset

- **Source**: UCI Machine Learning Repository
- **Features**: 11 physicochemical inputs (e.g., alcohol, sulphates, citric acid)
- **Target**: Wine quality score (integer rating)

Example:

| Fixed Acidity | Volatile Acidity | ... | Alcohol | Quality |
|---------------|------------------|-----|---------|---------|
| 7.4           | 0.70             | ... | 9.4     | 5       |

---

## 🧠 Models Used

- Linear Regression / Logistic Regression
- Random Forest
- Gradient Boosting (XGBoost)
- Support Vector Machines (optional)
- Hyperparameter tuning via GridSearchCV

---

## 📈 MLflow Tracking

MLflow is used to:
- 📌 Track parameters, metrics, and model artifacts
- 📦 Save and version models
- 📋 Compare runs using the MLflow UI
- 📍 Register best-performing model in the model registry

To launch the MLflow tracking UI:

```bash
mlflow ui
