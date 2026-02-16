# 🏠 House Price Prediction – Machine Learning Project  
**Master 2 MAS – Final Project**

## 📌 Project Overview

This project aims to predict real estate prices in India using supervised machine learning techniques.  
The objective is to compare several regression models and select the best-performing one using cross-validation and hyperparameter tuning.

The project follows a structured experimental pipeline:

1. Exploratory Data Analysis (EDA)  
2. Data preprocessing  
3. Train/validation split  
4. Model selection and hyperparameter tuning  
5. Performance evaluation and critical discussion  

---

## 📊 Dataset

- **Source:** MachineHack – House Price Prediction Challenge (2020)  
- **Problem type:** Supervised regression  
- **Target variable:** `PRICE_IN_LACS`  
- **Features include:**
  - Numerical variables (area, bedrooms, bathrooms, etc.)
  - Categorical variables (city, address)
  - Geographical coordinates (latitude, longitude)

The goal is to predict housing prices based on structured tabular data.

---

## 🔎 Exploratory Data Analysis

Key findings from the EDA:

- The target variable is **right-skewed**, justifying the use of RMSLE.
- Location-based features strongly influence price.
- Presence of high-end outliers in the dataset.
- Non-linear relationships suggest tree-based models are more suitable than linear models.

---

## 🤖 Models Evaluated

The following models were trained and compared:

- **Ridge Regression** (baseline linear model)
- **Random Forest Regressor**
- **ExtraTrees Regressor**
- **CatBoost Regressor** (gradient boosting with native categorical handling)

Hyperparameters were optimized using **RandomizedSearchCV** with cross-validation.

---

## 📈 Evaluation Metric

The primary evaluation metric is:

### RMSLE — Root Mean Squared Logarithmic Error

RMSLE was chosen because:

- It is more robust to outliers than RMSE.
- It measures relative (percentage-like) error.
- It is well-suited for skewed price distributions.

---

## 🏆 Final Model

The best-performing model was selected based on cross-validation and validation set RMSLE.

Tree-based ensemble methods significantly outperform linear regression due to their ability to capture complex non-linear interactions between features.

---

## 🧠 Discussion & Insights

- Ensemble models reduce variance and improve generalization performance.
- CatBoost effectively handles categorical variables without extensive preprocessing.
- A slight train/validation gap suggests moderate variance but no severe overfitting.
- Further improvements could include:
  - Advanced feature engineering
  - Target encoding strategies
  - Model stacking or blending
  - Extended hyperparameter search
  - 5-fold cross-validation for increased robustness

---

## ⚙️ Reproducibility

To reproduce the results:

```bash
git clone https://github.com/AyoubAchourIT/House-Price-Prediction-Challenge.git
cd House-Price-Prediction-Challenge
```
### Open

- `Projet_ML_M2MAS_HousePrice_India.ipynb`

### Then run

- `Kernel → Restart & Run All`

---

## 🛠 Requirements

- Python 3.9+
- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn
- catboost

---

## 👤 Author

**Ayoub ACHOUR**  
Master 2 MAS – Université Clermont Auvergne  
2026

