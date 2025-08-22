# stocks-prediction-with-ML
Stock Price Forecasting with Machine Learning: Multilayer Perceptron, Support Vector Regression, Random Forrest, Extreme Gradient Boosting
In this repository, the main objective is to compare four machine learning models and their accuracy forecasting three well-known stocks traded in the NYSE (TSLA, APPL, NVDA) in the short-term over the period March 2020 to May 2022. I deploy, develop, and hypertune XGBoost, Random Forest, Multi-layer Perceptron, and Support Vector Regression models and report the models that produce the highest accuracies from our evaluation metrics: RMSE, MAPE, and MPE. After using 240 training days, it can be concluded that XGBoost gives the highest accuracy despite taking longer than the rest to run.

A. Feature Engineering: To have a uniform format, this study focuses on the timeframe of March 2020 to May 2022. In addition to the 8 numerical variables mentioned below, dummy time variables will also be added into the machine learning models to capture calendar effects and seasonality patterns on stock prices. Separate studies will be performed for each target variable with the same exogenous variables. A summary of the variables that I believe can affect stock prices can be seen below.

1. Numerical Variables
o Price of Two-year treasury bond
o Price of Five-year treasury bond
o Price of Ten-year treasury bond
o Value of Dow Jones Index
o Value of Nasdaq Index
o Value of S&P 500 Index
o Price of Gold
o Price of Oil

2. Time Variables (dummy)
o Months of the year (12 variables)
o Day of the month (31 variables)
o Week day (5 variables for Monday to Friday)
o Hours of the day (6 variables for hours 9 to 16)
o Minute Segment of the hour (4 for minute segment 0, 15, 30, and 45)
o Whether the time period is in Monday morning (1 variable) o Whether the time period is in Friday afternoon (1 variable)
o Whether the time period is in a ”Pre-holiday” afternoon (1 variable)
o Whether the time period is in a ”post-holiday” morning (1 variable)

3. Target Variables
o Price of Tesla Stock; Target Variable 1
o Price of Apple Stock; Target Variable 2
o Price of Nvidia Stock; Target Variable 3

B. Normalization: The min-max normalization process is applied across all numerical variables to lessen the effects of outliers on the overall dataset.

C. Performance Evaluation

After running the machine learning models, we must evaluate how accurate the forecasts are. In this research, there are a total of 4 accuracy measures to evaluate the performance of the machine learning models: Root mean squared error (RMSE), Mean absolute percentage error (MAPE), Mean positive error (MPE), and Mean train time (MTT). These metrics are usually used to assess the performance of machine learning models on time series data.

Conclusion: After deploying and hypertuning models, the outcome of this experiment showed that, although having the highest training time, XGBoost had the highest accuracy. It can also be concluded that the forecasts of the machine learning models are also more accurate during low volatility periods.
