# M5 middle out approach
A middle out approach to m5 competition that scored 0.63413 on the private leaderboard, which is a top 5% solution

I used the scikit library https://scikit-hts.readthedocs.io/en/latest/ to create the hierarchy and the main dataframe

The solution is a blend of a Holt winters exponential smoothing model, an ARIMA model with exogenous variables and a tuned Prophet model.

These models were used to forecast at the department level and above and were reconcilled with a weighted least squares estimator using variance scaling, as described in this book https://otexts.com/fpp2/reconciliation.html

The department level forecasts were then projected down to the bottom level using the average historical proportions method. https://otexts.com/fpp2/top-down.html
