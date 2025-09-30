# Apple-Stock-Analysis-and-Forecasting-using-Multivariate-Regression

This project performs an exploratory data analysis (EDA) on Apple stock data obtained using the `yfinance` library, calculates technical indicators, and builds a forecasting model using Prophet and a Multi-Output Regression model.

## Project Overview

The main goal of this project is to analyze historical Apple stock price and volume data, identify potential trends and patterns using technical indicators, and forecast future closing prices.

## Data

The data used in this project is Apple stock data fetched for the last 2 years using the `yfinance` library. It includes:

- Open, High, Low, and Close prices
- Volume
- Dividends
- Stock Splits

## Analysis and Findings

The analysis included:

- **Data Loading and Inspection:** Initial loading and inspection of the data to understand its structure, identify missing values, and check for duplicates.
- **Descriptive Statistics:** Calculation of basic statistics for price and volume.
- **Time Series Visualization:** Plotting the closing price and volume over time to observe trends.
- **Seasonal Decomposition:** Decomposing the closing price time series to identify trend, seasonality, and residual components.
- **Technical Indicator Calculation:** Calculating and adding columns for:
    - 14-day Relative Strength Index (RSI)
    - 12-day Exponential Moving Average (EMA)
    - 26-day Exponential Moving Average (EMA)
    - 50-day Simple Moving Average (SMA)
    - 200-day Simple Moving Average (SMA)
- **Technical Indicator Analysis:** Analyzing the relationships and crossovers of SMAs and EMAs, and interpreting RSI values.
- **Correlation Analysis:** Visualizing the correlation matrix between different features.
- **Volatility and Volume Analysis:** Examining the relationship between daily returns, volatility, and trading volume.

## Forecasting

Two forecasting approaches were explored:

1.  **Prophet Model:** A Prophet model was trained to forecast the Apple stock closing price for the next year. The model's performance on historical data was evaluated using RMSE and MAE.
2.  **Multi-Output Regression with RandomForestRegressor:** A Multi-Output Regressor model with a RandomForestRegressor base estimator was trained to predict the closing price for the next 1, 5, and 10 days. The model was evaluated using MSE, RMSE, MAE, and R-squared.

## Project Structure

The notebook is structured into sections covering data loading, EDA, technical analysis, feature engineering, and modeling.

## Libraries Used

- `yfinance`
- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `statsmodels`
- `sklearn`
- `prophet`

## Getting Started

To run this notebook, you will need to have the necessary libraries installed. You can install them using pip:
