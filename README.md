# Apple-Stock-Analysis-and-Forecasting-using-Multivariate-Regression

This project performs an exploratory data analysis (EDA) on Apple stock data obtained using the `yfinance` library, calculates technical indicators, and builds a forecasting model using Prophet and a Multi-Output Regression model.

## Project Overview

The main goal of this project was to analyze historical Apple stock price and volume data, identify potential trends and patterns using technical indicators, and forecast future closing prices.

## Data

The data used in this project is Apple stock data fetched for the last 2 years using the `yfinance` library. It includes:

- Open, High, Low, and Close prices
- Volume
- Dividends
- Stock Splits

## Key Findings and Analysis

Through the analysis of Apple stock data, the following key findings were observed:

*   **Data Characteristics:** The dataset for the past two years is complete with no missing values or duplicates. The closing price ranged from approximately $163.82 to $258.10, with an average of around $207.69. Trading volume showed significant variability, with a maximum volume of over 318 million.
*   **Price and Volume Trends:** Visualizations of closing price and volume over time clearly showed the overall trends and fluctuations in the stock.
*   **Seasonal Decomposition:** Decomposing the closing price time series revealed underlying trend and seasonal components, providing insights into the cyclical patterns of the stock price.
*   **Technical Indicator Insights:**
    *   **Moving Averages (SMA 50/200 and EMA 12/26):** The analysis of moving averages indicated a potential bullish long-term trend (SMA 50 above SMA 200) and a potential bullish short-term trend (EMA 12 above EMA 26) at the time of the last data point. Crossover points were identified, suggesting potential shifts in momentum.
    *   **Relative Strength Index (RSI 14):** The 14-day RSI was calculated to be 69.69, indicating neutral momentum, close to the overbought threshold of 70.
*   **Correlation Analysis:** A correlation matrix visualized the relationships between different features, helping to understand which technical indicators and other data points moved together.
*   **Volatility and Volume Relationship:** Analysis showed a relationship between daily returns and volatility, and a comparison of average trading volume on days with large price movements versus normal days provided insights into market activity during significant price changes.

## Forecasting Models

Two forecasting approaches were implemented and evaluated:

1.  **Prophet Model:** A Prophet model was trained to forecast the Apple stock closing price for the next year. The model achieved a Root Mean Squared Error (RMSE) of 5.64 and a Mean Absolute Error (MAE) of 4.37 on the historical data used for training.
2.  **Multi-Output Regression with RandomForestRegressor:** This approach utilizes a Multi-Output Regression model with a RandomForestRegressor as the base estimator. Multi-Output Regression is a technique used when a single model needs to predict multiple target variables simultaneously. In this project, the model was trained to predict the closing price for three future time horizons: the next 1 day, the next 5 days, and the next 10 days. The model was evaluated using Mean Squared Error (MSE) of 18.58, a Root Mean Squared Error (RMSE) of 4.31, a Mean Absolute Error (MAE) of 3.23, and an R-squared (R2) score of 0.92 on the test set.
![Actual vs Predicted Prices](actual_vs_predicted_prices (1).png)
These results indicate that both models show promise in forecasting Apple stock prices, with the Multi-Output Regression model demonstrating a strong R-squared value on the test data for short-term predictions.

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
