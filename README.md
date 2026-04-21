# APPLE-STOCK-PREDICTION-WITH-NLP.

# Apple Stock Price Prediction Project

This notebook demonstrates a basic stock price prediction analysis for Apple (AAPL) using historical data fetched with `yfinance`.

## Project Overview

1.  **Data Acquisition**: Fetched 6 months of historical Apple stock data using the `yfinance` library.
2.  **Exploratory Data Analysis (EDA)**:
    *   Examined the first few rows of the dataset.
    *   Checked for missing values and data types.
    *   Plotted the closing price over time.
    *   Calculated daily percentage change.
    *   Generated descriptive statistics.
3.  **Feature Engineering**:
    *   Calculated 7-day and 30-day moving averages (`MAV_7`, `MAV_30`).
    *   Calculated 7-day rolling volatility (`volatality`).
    *   Created a 'days' feature to represent the time elapsed since the start of the data, converting date information into a numerical format suitable for regression models.
4.  **Model Building and Training**:
    *   **Linear Regression**: A simple linear regression model was built and trained to predict the closing price based on the 'days' feature.
    *   **Polynomial Regression**: A polynomial regression model (with degree 4) was built and trained using a pipeline (`PolynomialFeatures` and `LinearRegression`) to capture non-linear relationships.
5.  **Model Evaluation**: Both models were evaluated using `mean_absolute_error`, `mean_squared_error`, `root_mean_squared_error`, and `r2_score`.
6.  **Model Comparison**: The performance of the Linear Regression and Polynomial Regression models was compared.

## Key Findings

*   **Data Characteristics**: The dataset covers approximately 6 months of Apple stock data, showing various price movements, moving averages, and volatility over time.
*   **Model Performance**:
    *   **Linear Regression**:
        *   Mean Absolute Error (MAE): 6.1469
        *   Mean Squared Error (MSE): 54.7885
        *   Root Mean Squared Error (RMSE): 7.4019
        *   R-squared (R2): 0.1664
    *   **Polynomial Regression (Degree 4)**:
        *   Mean Absolute Error (MAE): 4.6415
        *   Mean Squared Error (MSE): 38.5180
        *   Root Mean Squared Error (RMSE): 6.2063
        *   R-squared (R2): 0.4139

**Conclusion**: The Polynomial Regression model (Degree 4) performed better than the Linear Regression model, exhibiting a higher R-squared value and lower error metrics. This suggests that a non-linear relationship exists between the 'days' feature and the closing price of Apple stock, which the polynomial model was better able to capture.

## Important Disclaimer

This project is for educational and demonstrative purposes only. It is a simplified analysis based on limited data and features. Stock market predictions are inherently complex and uncertain. Past performance is not indicative of future results. **This analysis does not provide financial advice or recommendations on investing in Apple stocks.** For any investment decisions, always consult with a qualified financial advisor.
