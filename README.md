# Forex_Trading_w_Machine_Learning
* The foreign exchange (also known as FX or forex) market is a global marketplace for exchanging national currencies.
* Currencies trade against each other as exchange rate pairs. For example, EUR/USD is a currency pair for trading euro against the US dollar.
* Forex markets exist as spot (cash) markets as well as derivatives markets offering forwards, futures, options, and currency swaps.
* Market participants use forex to hedge against international currency and interest rate risk, to speculate on geopolitical events, and to diversify portfolios, among several other reasons.

## Problem Statement
forecast forex pair pricing with time-series machine learning models.

## Dataset Information
For each of the Forex Pair, the dataset consist of the following columns:
* Date -  Date of the transaction record 
* Time – Opening/Starting time of the transaction record 
* Opening – Opening price of time period
* High – Highest recorded price within the time period
* Low – Lowest recorded price within the time period
* Close -  Closing price of the time period
* Volume – Transacted volume within the time period

## Time Series Data
Time series data is a collection of observations obtained through repeated measurements over time. Plot the points on a graph, and one of your axes would always be time.

* Time series data can be useful for:
* Tracking daily, hourly, or weekly weather data
* Tracking changes in application performance
* Medical devices to visualize vitals in real time
* Tracking network logs


## Problem Description 
* Before starting actual analysis
* First of all we will be do data processing
* Visualization of the Dataset
* Regression Models Evaluation
* Important Concept/Properties ofTime Series Analysis


## modeling method
* Smoothing Effect of Moving Average
* Weighted Exponential Smoothing
* Exponential and Double Exponential Smoothing
* Seasonality - Repeating Trends
* Stationary vs Non-Stationary Data

## Datetime Series Analysis Forecasting Models!
Time Series Analysis with Statsmodels
* Holt-Winters Method
Time Series Forecasting Model:
* ARIMA (p,d,q)
* SARIMA(p,d,q) (P,D,Q)
* Seasonal Autoregression Average Model, seasonal component (P,D,Q)
* SARIMAX
* SARIMA model that support supports exogenous regressor variables

## Explaination of Holt-Winters Method:
* This feature of the model allows us to quickly build anomaly detection systems, even for noisy series data, without spending too much time and money on preparing the data and training the model.
* It was first suggested by C.C. Holt in 1957 and was meant to be used for non-seasonal time series showing no trend. He later offered a procedure (1958) that does handle trends. 
Winters(1965) generalized the method to include seasonality, hence the name "Holt-Winters Method".
* The Holt-Winters Method has 3 updating equations, each with a constant that ranges from 0 to 1. The equations are intended to give more weight to recent observations and less weights to observations further in the past.
* These weights are geometrically decreasing by a constant ratio.
* The HW procedure can be made fully automatic by user-friendly software.

## Explaination of White Noise
* White noise is an important concept in time series forecasting.
* If a time series is white noise, it is a sequence of random numbers and cannot be predicted. 
* If the series of forecast errors are not white noise, it suggests improvements could be made to the predictive model![white noice](https://user-images.githubusercontent.com/74976732/126274124-b88859f1-72b2-41c0-a42a-7a2a8625ff1d.jpg)

## ARIMA Models
* ARIMA model formed by 3 components (3 parameters)
* AR - AutoRegression
* I - Integrated
* MA - Moving Average
* AR – AutoRegression (Parameter p = number of time lags)
* The AR part of ARIMA indicates that the evolving variable of interest is regressed on its own lagged (i.e., prior) values.

* I – Integrated (Parameter d = degree of differencing)
* Indicates that the data values have been replaced with the difference between their values and the previous values

* MA - Moving Average (Parameter q = order of the moving average)
* Indicates the regression error is actually a linear combination of error terms whose values occurred contemporaneously and at various times in the past. ![image](https://user-images.githubusercontent.com/74976732/126274173-675ae0a8-3e94-4f90-8107-2a1766bd0e3f.png)


## SARIMAX Models
We engineered the following additional features as exogenous regressor variables
We have 36 different combinations created from the 6 SARIMA parameters. 
We tried each combination and trained SARIMA with each so to find the best performing model. 
![image](https://user-images.githubusercontent.com/74976732/126273847-929a3f0b-3f09-4e10-bfab-a19ee00c4eb4.png)
## SARIMAX retrain model on full data, and forecast the future
![image](https://user-images.githubusercontent.com/74976732/126274599-c6107a9f-a718-4577-af7b-81d82c82d796.png)

## Challenges and Limitation
Forex prices changes are affected by many factors actually, our model has not able to factor all foreseeable repeated seasonal trend, example:
* Scheduled economical government announcement (like non-farm employment rate by US)
* Respective countries’ holidays

The model we worked on was based on historical data imported from csv file, it will be better if we can get live data to get most recent dataset 

