# Rainfall-Prediction--Kerala
Rainfall Prediction using ARIMA Time Series Model

Autoregressive Integrated Moving Average (ARIMA) is one of the most popular technique for time series modeling.
This is also called Box-Jenkins method, named after the statisticians who pioneered some of the latest developments on this
technique.

An ARIMA model can contain following  components. However, not all models need to have all of the below mentioned components.
1. Autoregressive (AR)  - Value of a time series at time period t (yt) is a function of values of time series at previous time                              periods ‘p’
2. Integrated (I) - This is required in making a time series Stationary and is represented by 'd' term in ARIMA.Basically this a                     differencing term where we take a difference of successive term and use it in modelling.
3. Moving Average (MA) - Value of a time series at time period t (yt) is a function of errors at previous time periods ‘q’


Generally a time series should be stationary before used for modelling. We can do it manually by making some log transformations or differencing. The 'd' term in ARIMA model takes care of it automatically.

Here, we are going to look at a more sophisticated time series model called as Auto ARIMA which is identical to the package in R. The Beauty of this package is that it automatically makes the time series stationary and comes up with the optimal values of p,d and q.

A good time series model should have the below ideal properties.

1. Residuals shouldn’t show any trends over time.

2. Auto correlation Factors(ACF) and Partial Auto correlation Factor (PACF) shouldn’t have large values (beyond significance level)for any lags. ACF indicates correlation between the current value to all the previous values in a range. PACF is an extension of ACF, where it removes the correlation of the intermediate lags. You can read more on this here.

3. Errors shouldn’t show any seasonality

4. Errors should be normally distributed

5. Error (MAE, MSE etc.) should be low

6. AIC, BIC should be relatively lower compared to other alternative models.
