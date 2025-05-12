Time Series Analysis for Sale Prediction

---
This repository contains a Python script that performs time series analysis on a dataset to predict future sales. The analysis includes data preprocessing, feature engineering, and the application of various machine learning models.

## Table of Contents

- [Introduction](#introduction)
- [Dataset](#dataset)
- [Installation](#installation)
- [Models](#models)
- [Results](#results)

## Introduction

The goal of this project is to analyze historical sales data and build predictive models to forecast future sales. The analysis involves:
1. Exploratory data analysis (EDA)
2. Feature engineering
4. Model training and evaluation

## Dataset

The dataset used in this project is `sales_data.csv`, which contains historical sales data with the following columns:

- `date`: Date of the sale
- `store`: Store ID
- `item`: Item ID
- `sales`: Number of items sold

## Installation

To run the code, ensure you have Python 3.x installed along with the required libraries. You can install the necessary packages using pip:

```bash
pip install pandas numpy matplotlib scikit-learn statsmodels torch darts
```


## Models

The following machine learning models are implemented in this analysis:

- NaiveSeasonal
- ARIMA
- AutoARIMA
- XGBModel
- Prophet
- ExponentialSmoothing
- LSTM (torch)

Each model's performance is evaluated using Mean Absolute Percentage Error (MAPE)

## Results
| Rank | Model                  | MAPE  |
|------|------------------------|-------|
| 1    | **LSTM**               | **22.42** |
| 2    | **XGB with covariates**| **22.77** |
| 3    | Prophet                | 23.49 |
| 4    | XGB                    | 25.81 |
| 5    | ExponentialSmoothing   | 28.97 |
| 6    | ARIMA                  | 31.13 |
| 7    | naive_365              | 33.92 |
| 8    | combined               | 34.26 |
| 9    | naive_7                | 38.17 |
| 10   | AutoARIMA              |


