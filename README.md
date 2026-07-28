# Forecasting One-Month-Ahead S&P 500 Returns

This project examines whether macroeconomic predictors can improve one-month-ahead forecasts of S&P 500 returns. It compares OLS, Ridge, and Lasso regression with a historical-mean benchmark.

## Methodology

The analysis was completed in Python and includes:

- Downloading S&P 500 prices from Yahoo Finance and macroeconomic data from FRED
- Transforming predictors and adjusting for publication timing
- Testing predictors for stationarity using ADF and KPSS tests
- Selecting predictors using training-sample correlations and variance inflation factors
- Generating expanding-window forecasts with OLS, Ridge, and Lasso regression
- Evaluating performance using RMSE, MAE, directional accuracy, and out-of-sample R²
- Repeating the analysis across 60/40, 70/30, and 80/20 train–test splits

The final predictor set includes CPI inflation, the federal funds rate, the change in the term spread, the unemployment rate, and the credit spread. The dataset contains monthly observations from 2000 to 2025.

## Main Findings

The historical-mean benchmark produced the lowest forecast errors and the highest directional accuracy. OLS performed worst, while Ridge and Lasso improved on OLS but still failed to outperform the benchmark.

All three regression models produced negative out-of-sample R² values across the alternative train–test splits. The results suggest that the selected macroeconomic indicators provide little additional predictive value for one-month-ahead S&P 500 returns.

## Repository Contents

```text
README.md
sp500_return_forecasting.ipynb
sp500_return_forecasting.pdf
```
