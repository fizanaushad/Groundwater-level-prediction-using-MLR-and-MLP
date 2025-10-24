# Groundwater-level-prediction-using-MLR-and-MLP

## 📌 Project Overview
This project compares **Multiple Linear Regression (MLR)** and **Multilayer Perceptron (MLP)** models for predicting **Groundwater Levels (GWL)** based on climatic, soil, and hydrological features. It aims to analyze how traditional statistical models perform against neural networks in capturing spatial–temporal water table variations.


## 🧩 Dataset Description
- **Target Variable:** `GWL_average` (Groundwater Level)
- **Predictors:**
  - Rainfall (`RF_average`)
  - Temperature (`t2m_value`)
  - Precipitation (`tp_value`)
  - Soil moisture (`swvl1_value`, `swvl2_value`)
  - Soil composition (`sand_pct`, `floamy_pct`, `f_clayey_pct`)
  - Lagged groundwater level (`GWL_lag1`)
  - Time trend (`time_index`)
- **Units:** Monthly data across multiple districts

---

## ⚙️ Methodology
1. **Data Preprocessing**
   - Missing value imputation
   - Outlier treatment using Winsorization
   - Lag feature creation and sorting by date

2. **Exploratory Data Analysis**
   - Summary statistics, correlation heatmaps, and pair plots

3. **Model Development**
   - **MLR:** Ordinary Least Squares regression using `statsmodels`
   - **MLP:** Neural Network regression using `sklearn.MLPRegressor`

4. **Model Diagnostics**
   - Residual analysis
   - Breusch–Pagan test (heteroscedasticity)
   - Durbin–Watson (autocorrelation)
   - Jarque–Bera test (normality)

5. **Performance Metrics**
   - Mean Absolute Error (MAE)
   - Mean Squared Error (MSE)
   - R² Score
   - Paired t-test/Wilcoxon for significance comparison

---

## 🧠 Results
| Model | MAE | MSE | R² | Observation |
|--------|-----|-----|----|--------------|
| MLR | Higher | Higher | Moderate | Good interpretability |
| MLP | Lower | Lower | Higher | Better pattern learning |

MLP achieved **better prediction accuracy** and captured nonlinear interactions more effectively than MLR.

---

## 🧰 Technologies Used
- Python 3
- Jupyter Notebook
- Libraries:
  - `numpy`, `pandas`, `matplotlib`, `seaborn`
  - `statsmodels`, `scipy.stats`, `sklearn`

---

## 📊 Applications
- Groundwater resource monitoring
- Climate–hydrology modeling
- Policy planning for water sustainability

---


