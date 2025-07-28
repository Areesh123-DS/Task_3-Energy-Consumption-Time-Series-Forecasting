# Task 3: Energy Consumption Time Series Forecasting

## 📌 Objective
Forecast short-term household energy usage using historical time-based patterns.

## 🛠️ Approach

### 1. ⏱ Time Series Preprocessing
- Parsed `Date` and `Time` into a unified datetime format
- Set datetime as index
- Resampled data to **hourly frequency** using `.resample('H')`

### 2. 🧠 Feature Engineering
- Extracted time-based features:
  - `hour`
  - `day_of_week`
  - `is_weekend` (boolean flag)

### 3. 📊 Model Comparison
Implemented and compared the following models:

| Model   | Type                |
|---------|---------------------|
| ARIMA   | Traditional time series model |
| Prophet | Additive time series forecasting (Meta/Facebook) |
| XGBoost | Machine learning model using engineered time features |

### 4. 📈 Evaluation Metrics
- **MAE (Mean Absolute Error)**
- **RMSE (Root Mean Squared Error)**

---

## 📉 Forecast Visualization
- Plotted **actual vs. predicted** values for all models
- Compared model performance over the last **30 days**

---

## 🔍 Results and Findings

| Model   | MAE   | RMSE  |
|---------|-------|-------|
| ARIMA   |0.6697 |0.8302 |
| Prophet |0.5605 |0.7270 |
| XGBoost |0.2341 |0.3464 |


---
- ✅ **XGBoost** significantly outperforms both ARIMA and Prophet in terms of **MAE** and **RMSE**.
- ✅ **Prophet** performs better than ARIMA, especially in handling seasonal patterns.
- ❗ **ARIMA**, while traditional, lags behind in accuracy for this dataset.
- 📉 Lower MAE and RMSE indicate **XGBoost is best suited** for short-term forecasting in this task.


## 📦 Libraries Used

- `pandas`, `numpy`
- `matplotlib`, `seaborn`
- `statsmodels` (for ARIMA)
- `prophet`
- `xgboost`
- `sklearn` (for evaluation metrics)

---

