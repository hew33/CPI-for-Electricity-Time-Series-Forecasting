# CPI-for-Electricity-Time-Series-Forecasting
Forecasting the 2020 CPI for electricity based on monthly CPI for electricity dataset with over 100 hundred years monthly records since 1913.
## Introduction
Electricity is very important energy of every person in this world. This project is aimed to forecast future electricity consumption in 2020. Data can be found on FRED at https://fred.stlouisfed.org/series/CUUR0000SEHF01
## Steps
1. Data Gathering, Assessing, and Cleaning
<br>      a. Rename the column with an appropriate name
<br>      b. Replace "." with NaN
<br>      c. Correct the wrong datatype of CPI_electricity into float
<br>      d. Fill the missing values by forward filling method
2. Exploration
<br>      a. Seasonal decomposition analysis
<br>      b. Build models, including ETS model and ARIMA model
3. Compare the models
<br>      a. Residual plots
<br>      b. Information criteria
<br>      c. Measures of error
4. Forecasting: Add train and test datasets together and forecast the next 12 months CPI for electricity
## Result
The CPI for electricity dataset has an approximately linear upward but slightly getting flat trend , seasonal pattern with a size of 12 months, and a more volatile residual in recent years. I tried the ETS model without damping and ETS without damping, the ETS model with damping, and ARIMA model.
ETS model with damping and ETS model without damping have similar AIC and BIC, and both a lot lower than those of ARIMA model, but the much lower error measures, including MAE, MSE, MAPE, MPE, ME, RMSE, indicates that ETS model without damping is the best model. 
