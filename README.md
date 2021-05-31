# HW-Time-Series-JPY-Prices-Return-Forecasting

## Background

We want to forcast JPY futures prices using: 

1. Time Series Forcasting
   1. ARMA - ARIMA
   2. GARCH
2. Linear Regression Modeling

# Time Series Conclusion
### The questions I tried to answer : 

1. Would you buy the yen now?
2. Is the risk of the yen expected to increase/decrease ?
3. Based on the model evaluation, would you feel confident in using these models for trading?

Based on both ARMA and ARIMA models, we would be tempted to buy the JPY as we expect the price to increase (from ARIMA analysis) and the expected returns to slightly decrease but overall staying flat for the next 5 days. 

From our volatility study using GARCH model, we can see that the model expects the volatility to increase over the next 5 days and hence predicts the risk to increase. 

However it is important to note that both ARMA and ARIMA models have a very high P value which shows a very low confidence in the models. ARMA model has only a 62% confidence level and ARIMA model shows a 45% confidence level. 
The GARCH model however shows a P value below 0.05 benchmark (with an actual 97% confidence). The beta coefficient of the GARCH model is also relatively high at 0.95 (close to 1) - this indicates that a change in today's volatility will significantly impact the folowing period volatility. Therefore I would not feel confident to use these models for real trading. 

We can conclude that we are pretty confident that the volatility of JPY prices will increase in the next 5 days. The models forcast a price increase for the same period but with a low confidence level. I would not buy the JPY yet but i would buy a volatility product like a straddle or strangle (options vol strategies) to benefit from the predicted rise of risk. 

# Linear Regression Conclusion

### The questions I tried to answer : 
1. Does this model perform better or worse on out-of-sample data compared to in-sample data?

By analysing the results of the linear regression, we can conclude that our model performs better on "out-sample" data compare to "in-sample" data. It is unusual to witness this as linear regression models tend to perform better on data it has already "seen" ("in-sample" data).  
The Out-of-Sample Root Mean Squared Error (RMSE)= 0.41 while the In-sample RMSE = 0.6 which is a significant difference. the closer the RMSE to 0 is the better the proformance is. 