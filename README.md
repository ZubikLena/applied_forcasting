# Applied Forecasting Project

This repository contains a **time-series forecasting pipeline**. The goal of the project is to predict **future product demand** based on historical sales data using machine learning techniques. The workflow includes **data preparation, exploratory data analysis (EDA), feature engineering, and demand forecasting using gradient boosting models**.


# Project Overview

The project builds a forecasting model capable of predicting **28-day future demand** for retail products. The pipeline follows a standard machine learning forecasting workflow:

1. Data merging and preprocessing
2. Exploratory data analysis and trend inspection
3. Feature engineering for time-series forecasting
4. Model training and validation
5. Forecast generation

The final model predicts future sales using **lag-based time-series features and gradient boosting regression**.


# Methodology

## Trend Analysis

Exploratory data analysis was performed to understand patterns in the data, including:

* overall sales trends over time
* weekly and monthly seasonality
* event and holiday effects
* price influence on demand

Visualization tools were used to detect:

* long-term trends
* seasonal patterns
* irregular fluctuations


# Forecasting Model

The prediction model is based on:

**Histogram-based Gradient Boosting Regression**

```python
HistGradientBoostingRegressor
```

This algorithm was chosen because:

* it handles nonlinear relationships well
* it works efficiently with tabular features
* it performs well on structured time-series data
* it is computationally efficient for large datasets

The model learns the relationship between engineered features and future demand.


# Forecasting Strategy

The forecasting pipeline uses **recursive multi-step forecasting**:

1. Train the model on historical data
2. Predict the next day’s demand
3. Append the prediction to the dataset
4. Use predicted values as future lag features
5. Repeat until the **28-day forecast horizon** is reached

This approach allows the model to generate **multi-step forecasts using a single trained model**.


# Repository Structure

```
master_data.ipynb
eda.ipynb
submission.ipynb
```


# Tools & Libraries

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn

Key model:

* `HistGradientBoostingRegressor` (Scikit-learn)

---

# Key Concepts Demonstrated

* time-series feature engineering
* machine learning forecasting
* recursive multi-step prediction
* backtesting of forecasting models
* demand prediction using gradient boosting
