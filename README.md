# 📈 Stock Market Analysis ML

This project focuses on **stock market analysis and prediction** using a dataset containing historical stock prices. The workflow includes data preprocessing, exploratory data analysis (EDA), and the implementation of multiple machine learning models to forecast **stock closing prices**.

---

## 🚀 Project Overview

The primary goal is to **analyze stock data, identify trends, and develop accurate predictive models**.  
The project utilizes **time-based features** and common regression algorithms to predict the `Close` price of the stock.

### 🔑 Key Steps
- **Data Loading & Preprocessing**  
  - Import dataset, verify column types, handle missing values.
- **Feature Engineering**  
  - Extract temporal features from the `Date` column (Year, Month, Day, DayOfWeek, DayOfYear).
- **Exploratory Data Analysis (EDA)**  
  - Visualize the closing price trend over time.
- **Model Building**  
  - Train three regression models: LightGBM, Random Forest, XGBoost.
- **Model Evaluation & Comparison**  
  - Assess performance using R² Score, MAE, and RMSE.

---

## 💾 Dataset

The project is based on a **generic stock dataset** (fetched or simulated) with the following structure:

| Column       | Description                        |
|--------------|------------------------------------|
| Date         | Trading date                       |
| Open         | Opening price of the stock         |
| High         | Highest price of the day           |
| Low          | Lowest price of the day            |
| Close        | Closing price of the stock         |
| Volume       | Number of shares traded            |
| Adj Close    | Adjusted closing price             |

---

## 🛠️ Libraries Used

- **Core Libraries**
  - `pandas`
  - `numpy`

- **Visualization**
  - `matplotlib`
  - `seaborn`
  - `plotly.express`

- **Machine Learning & Metrics**
  - `scikit-learn`  
    - `train_test_split`  
    - `mean_absolute_error`  
    - `mean_squared_error`  
    - `r2_score`
  - `lightgbm`
  - `xgboost`

- **Utilities**
  - `glob`

---

## ✨ Analysis & Results

### 1. Stock Price Trend
- The closing price shows a clear **upward trend** over time.  
- This trend makes forecasting easier for models that capture **non-linear relationships**.

### 2. Model Performance

| Model         | R² Score | MAE   | RMSE  |
|---------------|----------|-------|-------|
| LightGBM      | 0.999    | 0.286 | 0.354 |
| Random Forest | 0.998    | 0.407 | 0.609 |
| XGBoost       | 0.999    | 0.284 | 0.350 |

**Interpretation:**
- All three models achieved **excellent performance** with R² scores close to 1.0.  
- **XGBoost** performed best with the lowest MAE and RMSE.  
- The very low error suggests that predicting the next day's price is relatively simple when using **time-based features** and **tree-based algorithms**.

### 3. Visual Comparison of Forecasts
- Predictions from all models closely track the actual closing prices.  
- **XGBoost and LightGBM** overlap almost perfectly with the actual stock price, confirming their high accuracy.

---


## 📝 Conclusion

- The project successfully built **highly accurate models** for forecasting stock closing prices using temporal features.  
- **XGBoost** emerged as the **top performer** with the lowest error metrics.  
- The analysis highlights that:
  - Time features (date, month, day, etc.) are **highly correlated** with stock price trends.  
  - Tree-based ensemble methods are well-suited for capturing **non-linear relationships** in stock data.  
