
# 🕒 Time Series Analysis for Sales Prediction

This repository contains a Python-based pipeline for time series analysis and forecasting of sales data. The project includes data preprocessing, feature engineering, and implementation of several machine learning and deep learning models to predict future sales.

---

## 📚 Table of Contents

* [🔍 Introduction](##introduction)
* [📊 Dataset](##dataset)
* [⚙️ Installation](##installation)
* [🧠 Models Implemented](##models-implemented)
* [📈 Results](##results)

---

## 🔍 Introduction

The primary goal of this project is to analyze historical sales data and forecast future sales using a variety of time series models. Key steps include:

1. **Exploratory Data Analysis (EDA)**
2. **Feature Engineering**
3. **Model Training and Evaluation**

The project provides a comparative analysis of classical time series methods, machine learning approaches, and deep learning architectures.

---

## 📊 Dataset

The dataset used is `sales_data.csv`, which includes historical sales figures with the following columns:

* `date`: Date of the sale
* `store`: Store identifier
* `item`: Item identifier
* `sales`: Number of items sold

---

## ⚙️ Installation

To run the project, ensure Python 3.x is installed. Then, install the required packages using:

```bash
pip install pandas numpy matplotlib scikit-learn statsmodels torch darts
```

---

## 🧠 Models Implemented

This project evaluates a variety of models:

* 📉 **Statistical Models**

  * Naive (weekly and yearly seasonality)
  * ARIMA / AutoARIMA
  * Exponential Smoothing
  * Drift

* 📈 **Machine Learning**

  * XGBoost (with and without covariates)

* 🔮 **Hybrid / Specialized**

  * Prophet

* 🤖 **Deep Learning**

  * LSTM
  * Bi-LSTM (bidirectional)

---

## 📈 Results

Model performance is evaluated using **Mean Absolute Percentage Error (MAPE)**. Lower MAPE indicates better predictive performance.

| Rank | Model                       | MAPE (%)  |
| ---- | --------------------------- | --------- |
| 🥇 1 | **LSTM**                    | **22.03** |
| 🥈 2 | **Bi-LSTM**                 | **22.23** |
| 🥉 3 | **XGBoost with covariates** | **22.77** |
| 4    | Prophet                     | 23.49     |
| 5    | XGBoost                     | 25.81     |
| 6    | Exponential Smoothing       | 28.97     |
| 7    | ARIMA                       | 31.13     |
| 8    | Naive (yearly)              | 33.92     |
| 9    | Combined (ensemble)         | 34.26     |
| 10   | Naive (weekly)              | 38.17     |
| 11   | AutoARIMA                   | 39.53     |
| 12   | Drift                       | 68.74     |

