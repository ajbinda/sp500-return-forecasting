# Forecasting One-Month-Ahead S&P 500 Returns

This project examines whether macroeconomic predictors can improve one-month-ahead forecasts of S&P 500 returns. It compares OLS, Ridge, and Lasso regression with a historical-mean benchmark.

## Methodology

The analysis was completed in Python and includes:

- Downloading S&P 500 prices from Yahoo Finance and macroeconomic data from FRED
- Transforming predictors and adjusting for publication timing
- Testing predictors for stationarity using ADF and KPSS tests
- Selecting predictors using training-sample correlations, variance inflation factors, and economic intuition
- Generating one-step-ahead forecasts using 120-month rolling regression windows
- Using an expanding historical-mean benchmark
- Evaluating performance using RMSE, MAE, directional accuracy, and out-of-sample R²
- Repeating the analysis across 60/40, 70/30, and 80/20 train–test splits

The final predictor set includes CPI inflation, industrial production growth, the change in the federal funds rate, the change in the term spread, the change in the unemployment rate, and the change in the credit spread. The dataset contains monthly observations from 2000 to 2025.

## Main Findings

Ridge performed best in the 80/20 split, achieving approximately 1.5% out-of-sample R² and slightly outperforming the historical-mean benchmark. Ridge also produced a small positive out-of-sample R² of approximately 0.4% in the 70/30 split but underperformed the benchmark in the 60/40 split.

OLS and Lasso underperformed the historical-mean benchmark across all three splits. Overall, the results suggest that the selected macroeconomic indicators provide limited and inconsistent predictive value for one-month-ahead S&P 500 returns.

## Repository Contents

```text
README.md
paper_sp500_return_forecasting.pdf
source_sp500_return_forecasting.ipynb
```
