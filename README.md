### Time-Series-Forecasting-Linear-Regression-Forecasting
In this project, we will use time series forecasting and linear regression forecasting to predict future movements in the value of the Japanese yen versus the U.S. dollar.

#### Time-Series Forecasting

In this section, we will load historical Dollar-Yen exchange rate futures data and apply time series analysis and modeling to determine whether there is any predictable behavior.

We will complete the following:

1. Decomposition using a Hodrick-Prescott Filter (Decompose the Settle price into trend and noise).
2. Forecasting Returns using an ARMA Model.
3. Forecasting the Settle Price using an ARIMA Model.
4. Forecasting Volatility with GARCH.

Then, we will use the results of the time series analysis and modeling to answer the following questions:

1. Based on our time series analysis, should we recommend to buy the yen now?
2. Is the risk of the yen expected to increase or decrease?
3. Based on the model evaluation, are we confident in using these models for trading?

#### Linear Regression Forecasting

In this section, we will build a Scikit-Learn linear regression model to predict Yen futures ("settle") returns with *lagged* Yen futures returns and categorical calendar seasonal effects (e.g., day-of-week or week-of-year seasonal effects).

We will complete the following:

1. Data Preparation (Creating Returns and Lagged Returns and splitting the data into training and testing data)
2. Fitting a Linear Regression Model.
3. Making predictions using the testing data.
4. Out-of-sample performance.
5. In-sample performance.

We will then, use the results of the linear regression analysis and modeling to answer the following question:

* Does this model perform better or worse on out-of-sample data compared to in-sample data?

### Results

As we will see throughout this analysis, the quality of the analysis depends on the model used as well as on the quality of the data. Starting with time series analysis, the yen futures settle price plot shows that the Yen futures settle price fluctuates a lot due probably to some volatility as we can see from the plot, the settle price went from a high in 1996 to a bottom in around 1999-2000. Then, it started an upward trend again to another high around 2012 and from there to another bottom around 2016. It looks like that the Yen is heading to an upward trend again, however, it is not that high as of now.

The summary output of our ARMA model shows high P values, 3 of which are close to 1. Given the high values of P particularly, this ARMA model may be using an unreliable coefficient that might cause misleading results. Both lag 1 and lag 2 have negative impact with with negative coefficients. Also, the ARMA model 5 Day Stock Return Forecast plot shows a downward trend which flatned afterward. The ARIMA model also is showing high p values 5 of which are above the threshold however with the ARIMA model lag 1 and lag 2 have positive impact. Both the ARMA and the ARIMA are showing limitations on their reliability.
Based on my time series analysis, there is an increasing volatility and an upward trend of the Yen vs Dollars Settle price according to the results of the ARIMA and GARCH models. However when we look at the ARMA model the plot is showing a downward possibly flatning trend. There is high risk giving the increasing volatility and possibly high rewards too. 

From the linear regression modeling, based on the results we have our model is peforming better with out of sample testing than with the in-sample testing. It is good that the out of sample root mean square is lower than the in-sample root mean square, even though none of them is really close the zero. However when we compare the predicted values to the actual values, we see that in many instances the model is missing the trend and when it is correctly predicting the trend it is missing its extend, so this model needs to be retooled to make better predictions and be more reliable. 


