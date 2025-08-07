# 🏠 House Price Prediction using Machine Learning

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Scikit-learn](https://img.shields.io/badge/Scikit--Learn-%23FF9100.svg?logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-%23150458.svg?logo=pandas&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-%232E8B57.svg?logo=seaborn&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-%23150458.svg?logo=matplotlib&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-%23F37626.svg?logo=jupyter&logoColor=white)

A machine learning project to **predict house prices** based on key property features such as area, number of bedrooms, location, and amenities. This project uses regression models including **Linear Regression** and **Gradient Boosting**, with full preprocessing, evaluation, and visualization.

---

## 📌 Table of Contents
- [Overview](#overview)
- [Dataset](#dataset)
- [Features Used](#features-used)
- [Models Trained](#models-trained)
- [Preprocessing Steps](#preprocessing-steps)
- [Evaluation Metrics](#evaluation-metrics)
- [Results](#results)
- [Visualizations](#visualizations)

---

## 🔍 Overview

This project aims to build a predictive model for residential house prices using various structural and categorical features. The goal is to assist real estate platforms, buyers, and sellers in estimating property values accurately using data-driven insights.

The solution includes:
- Data exploration and cleaning
- Feature encoding and scaling
- Training and comparing two regression models
- Model evaluation using MAE and RMSE
- Visualization of predictions and feature importance

---

## 📁 Dataset

The dataset used is **"Housing.csv"**, commonly available on [Kaggle](https://www.kaggle.com/datasets/ashydv/housing-dataset). It contains 545 entries with the following key columns:
- `price`: Target variable (house price in INR)
- `area`: Built-up area in square feet
- `bedrooms`, `bathrooms`, `stories`: Number of rooms
- `mainroad`, `prefarea`, `airconditioning`: Binary location/amenity features
- `furnishingstatus`: Categorical (furnished, semi-furnished, unfurnished)
- `parking`: Number of parking spaces

---

## 🧩 Features Used

| Feature | Type | Description |
|-------|------|-------------|
| `area` | Numerical | Built-up area in sq. ft |
| `bedrooms` | Numerical | Number of bedrooms |
| `bathrooms` | Numerical | Number of bathrooms |
| `stories` | Numerical | Number of floors |
| `parking` | Numerical | Number of parking spots |
| `mainroad` | Binary | Proximity to main road |
| `prefarea` | Binary | Preferred residential area |
| `airconditioning` | Binary | Has AC or not |
| `furnishingstatus` | Categorical | Furnishing level |

---

## ⚙️ Preprocessing Steps

1. **Label Encoding** for binary features:  
   `mainroad`, `prefarea`, `airconditioning`
2. **Categorical Encoding** for `furnishingstatus` using `.cat.codes`
3. **Standardization** of all numerical features using `StandardScaler`
4. **Train-Test Split**: 80% training, 20% testing (`random_state=42`)

---

## 🤖 Models Trained

| Model | Description |
|------|-------------|
| **Linear Regression** | Baseline linear model |
| **Gradient Boosting Regressor** | Ensemble tree-based model with hyperparameter tuning |

---

## 📊 Evaluation Metrics

Both models were evaluated using:
- **Mean Absolute Error (MAE)**: Average absolute difference between predicted and actual prices
- **Root Mean Squared Error (RMSE)**: Emphasizes larger errors

---

## 📈 Results

| Model | MAE | RMSE |
|------|-----|------|
| **Linear Regression** | ₹23,75,000 | ₹30,40,000 |
| **Gradient Boosting** | ₹10,92,000 | ₹14,78,000 |

---

## 🖼️ Visualizations

### 1. Actual vs Predicted Prices
*Scatter plots comparing actual and predicted prices for both models.*

### 2. Feature Importance (Gradient Boosting)
*Top features influencing house prices: `area`, `bathrooms`, and `airconditioning` are most significant.*
