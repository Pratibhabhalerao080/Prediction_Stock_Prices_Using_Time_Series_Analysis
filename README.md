﻿# Stock Price Forecasting using ARIMA Model

This repository contains code for forecasting the stock price of Bajaj Finance Limited (BAJFINANCE) using the ARIMA (AutoRegressive Integrated Moving Average) model. We will use historical stock price data to build and evaluate the ARIMA model's forecasting performance.

## Prerequisites
Before running the code, ensure you have the following libraries installed:
- [pandas](https://pandas.pydata.org/): For data manipulation and analysis.
- [numpy](https://numpy.org/): For numerical operations.
- [pmdarima](https://pypi.org/project/pmdarima/): For automatic ARIMA model selection.

You can install the required libraries using pip:

```bash
pip install pandas numpy pmdarima
```

## Getting Started
1. Clone or download this repository to your local machine.

2. Open a Python environment (e.g., Jupyter Notebook) and navigate to the repository directory.

3. Run the `stock_price_forecast.py` script to execute the code.

## Usage
Here is a brief overview of the code and its functionality:

1. Data Loading:
   - The historical stock price data for Bajaj Finance (BAJFINANCE) is loaded from a CSV file using the `pandas` library.

2. Data Preprocessing:
   - The script performs various data preprocessing steps, such as setting the 'Date' column as the index, handling missing values, and creating lag features.

3. Lag Features:
   - Lag features are generated for the following columns: 'High', 'Low', 'Volume', 'Turnover', and 'Trades'. Rolling means and rolling standard deviations are computed for both 3-day and 7-day windows.

4. Model Building:
   - The script uses the `pmdarima` library to automatically select the best ARIMA model for forecasting the VWAP (Volume Weighted Average Price) of BAJFINANCE stock. The model is trained on the training data, including exogenous features created in the previous step.

5. Forecasting:
   - The ARIMA model is used to forecast the VWAP for a specified number of periods (485 days) on the testing data. The forecasted values are stored in the 'Forcast_ARIMA' column.

6. Visualization:
   - The script generates a plot to visualize the actual VWAP and the ARIMA forecast on the testing data.

7. Evaluation:
   - The code checks for any missing values in the testing data after forecasting.

## Disclaimer
Please note that this code is for educational and demonstration purposes only. Stock price forecasting is a complex task, and this code does not constitute financial advice. Always consult with financial professionals before making investment decisions.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

Feel free to modify and use the code according to your requirements.
