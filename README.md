## Time Series Forecasting on RBI data

### About the dataset
We went through the RBI website to find a dataset on CPI\
We found a dataset which had CPI values from Jan 2014 until Aug 2022

### Pre-processing
Since the data was from RBI, it was already cleaned therefore we didn't do any pre-processing\
We plotted graphs to visualize the data

### Model Building
We first decomposed the data to see if there was trend and seasonality\
We observed both trend and seasonality\
Therefore we differenced the data once which removed both trend and seasonality\
Since the data was made stationary we used ARIMA model to forecast\
Used 80:20 train test split to train the model

### Observations
We noticed that ARIMA model predicted values which were way different from test values