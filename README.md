# Prediction-on-US-Stock-Market-Performance

This is the code base for a data science project: Prediction on US Stock Market Performance (S&P 500).

## Introduction
In financial markets, traders and fund managers often aim to construct a simple and robust model to predict the US S&P 500 performance. There are two types of indicators: leading indicators and lagging indicators. Leading indicators are factors that change before the financial market changes (e.g., ISM manufacturing index, ISM non-manufacturing index, consumer sentiment), while lagging indicators respond some time after an exogenous shock (e.g., employment data, GDP). Due to time constraints, the scope of this project is narrowed down to focus on predicting the equity market from three other markets — energy, bullion, and bonds. The problem of interest is to predict returns on the S & P 500 index using indicators from these three markets. EDA results show evidence of cross-correlation and Granger causation between S&P 500 log return and other variables (crude oil futures log return, gold futures log return, change in 3-month treasury bill yield, and change in 10Y-3M treasury yield spread), making them promising predictors of the stocks.

For this project, the data frequency is weekly with data from November 10, 2002 to October 31, 2021 as the estimation sample, and data from November 7, 2021 to October 30, 2022 as the prediction period (test set). The forecasting scheme is fixed (rather than recursive or rolling) and the forecasting horizon is 3-step ahead. Three models are selected as the baseline: historical mean, last period naive, and autoregression. To improve on the baseline models, vector autoregression (VAR) and long short-term memory (LSTM) models are built and evaluated. 

## Usage
Code is contained in ./notebook directory. Run the ipynb notebook to reproduce the results.

## License
This project is licensed under the MIT License. Feel free to use, modify, and distribute the code according to the terms specified in the license.