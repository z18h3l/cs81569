java c
AD 685 Project – Fall 2024 
Instructions: 
· Type your response in a separate “word doc” named LastName_FirstName.doc  
· Also, you must upload the work files from R. I do not accept “.Rmd” format, so please convert everything into raw R file. 
· Do not use the forecast, quantmod, tseries or the strucchange package, AIC or BIC or arima function or basically, any packages that were not covered in the lecture. You will not receive any score for responses associated with these packages. If you are not sure, please consult me first before your submission. 
· Upload 3 files (Word doc and 3 R files) on Blackboard 
This project consists of two parts: 
· Part 1: Forecasting models for the rate of inflation. 
· Part 2: Cointegration Investigation and Vector Error Correction Model 
Part 1 
Forecasting models for the rate of inflation - Guidelines 
Go to FRED’s website (https://fred.stlouisfed.org/) and download the data for:
· Consumer Price Index for All Urban Consumers: All Items (CPIAUCSL) - Seasonally adjusted – Monthly Frequency – From 1947:M1 to 2017:M12
In this hands-on exercise you will construct forecasting models for the rate of inflation, based on CPIAUCSL.
For this analysis, use the sample period 1970:M01–2012:M12 (where data before 1970 should be used, as necessary, as initial values for lags in regressions).
a.
(i) Compute the (annualized from month-over-month change) inflation rate for each month.
(ii) Plot the value of Infl from 1970:M01 through 2012:M12. Based on the plot, do you think that Infl has a stochastic trend? Explain.
b.
(i) Compute the first twelve autocorrelations of (Infl and ΔInfl)
(ii) Plot the value of ΔInfl from 1970:M01 through 2012:M12. The plot should look “choppy” or “jagged.”  Explain why this behavior. is consistent with the first autocorrelation that you computed in part (i) for ΔInfl.
c.
(i) Compute Run an OLS regression of Inflt on Inflt-1. Does knowing the inflation this month help predict the inflation next month? Explain.
(ii) Estimate an AR(2) model for Infl. Is the AR(2) model better than an AR(1) model? Explain.
(iii) Estimate an AR(p) model for p = 0, ..., 8. What lag length is chosen by BIC? What lag length is chosen by AIC?
(iv) Use the AR(2) model to predict “the level of the inflation rate” in 2013:M01—that is, Infl2013:M01.
d.
(i) Use the ADF test for the regression in Equation (15.32) with two lags of ΔInfl to test for a stochastic trend in Infl. Does the Inflation rate have a units root?
(ii) Is the ADF test based on Equation (15.32) preferred to the test based on Equation (15.33) for testing for stochastic trend in ? Explain.
(iii) In (i) you used two lags of ΔInfl. Should you use more lags? Fewer lags? Explain.
(iv) Based on the test you carried out in (i), does the AR model for Infl contain a unit root? Explain carefully. (Hint: Does the failure to reject a null hypothesis mean that the null hypothes代 写AD 685 Project – Fall 2024R
代做程序编程语言is is true?)
e. Use the QLR test with 15% trimming to test the stability of the coefficients in the AR(2) model for “the inflation” Infl. (You cannot use the strucchange package. You must demonstrate, through your code, the procedure of a QLR test) Is the AR(2) model stable? Explain.
f.
(i) Using the AR(2) model for Infl with a sample period that begins in 1970:M01, compute pseudo out-of-sample forecasts for the inflation beginning in 2005:M12 and going through 2012:M12.  
(ii) Are the pseudo out-of-sample forecasts biased?  That is, do the forecast errors have a nonzero mean?
(iii) How large is the RMSFE of the pseudo out-of-sample forecasts? Is this consistent with the AR(2) model for Infl estimated over the 1970:M01–2005:M12 sample period?
Part 2 
Investigation of Cointegration Within the Stock Market 
Item (a) 
From the Time Series lectures, you learned that when two non-stationary time series share a stationary linear combination, they are said to be cointegrated. When exogenous shocks temporarily disturb this equilibrium relationship, the series tend to revert to their long-run pattern through an error correction mechanism. This mean-reversion property has been widely exploited by investment professionals as the foundation for pairs trading strategies. In this exercise, you will select two stocks or financial instruments that you believe to be economically related (e.g., companies in the same industry or with similar business models) and apply the Engle-Granger cointegration test to evaluate whether they are suitable candidates for a pairs trading strategy.
1) Pick two U.S. Stocks or financial instrument that you believe to be cointegrated and want to examine their feasibility for pair-trading. State the rationale AND elaborate of why you choose these two stocks. Here are some considerations or ideas on informing this decision:
a. Choose two companies that compete in the same market where they earn revenue from the same segment/group of end-users.
b. From the list of SP 500 constituents, choose two companies within the same GICS sector.
2) Download the historical monthly stock return (10-Year) from Yahoo Finance.
3) When conducting the Engle-Granger Augmented Dickey-Fuller test, you should assume that you do not know the cointegrating coefficient between the stocks’ return. Therefore, you will need to perform. a linear regression and estimate the residual.
In your write-up, please explain if two stock return series are cointegrated, how you will devise a pair-trading strategy to profit from a pattern drift? You must illustrate in drawing of how the strategy will profit or you will receive zero points for this portion of the project.
Item (b)
Using the two integrated stocks that you identified from Item (a), construct a Vector Error Correction model (VECM) to predict the next period’s stock return (or price). Calculate the RMSFE for the VECM.

         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
