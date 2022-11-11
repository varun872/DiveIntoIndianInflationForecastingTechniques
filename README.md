## Time Series Forecasting on RBI data

### About the dataset
We went through the RBI website to find a dataset on CPI\
We found a dataset which had CPI values from Jan 2014 until Aug 2022

### Pre-processing
Since the data was from RBI, it was already cleaned therefore we didn't do any pre-processing\
We plotted graphs to visualize the data

### Model Building 1 - ARIMA
We first decomposed the data to see if there was trend and seasonality\
We observed both trend and seasonality\
Therefore we differenced the data once which removed both trend and seasonality\
Since the data was made stationary we used ARIMA model to forecast\
Plotted the <strong>acf</strong> and <strong>pacf</strong>\
We got <strong>p</strong> value as 1 and <strong>q</strong> value as 1 visualizing the plots\
Used 80:20 train test split to train the model

### Observations
The Ljung-Box test value smaller than 0.05 which suggested that the model was not accurate\
We noticed that ARIMA model predicted values which were way different from test values\
Plotted graph of the predicted values with the original values showed a straight line which implied that the prediction was incorrect

### Model Building 2 -SARIMA
We have used auto_arima function from pmdarima library which finds the best sarima model for the given data and returns the model.\
The best SARIMA parameters we got using the above function has order = (2,1,0) and seasonal_order=(0,1,2,12).\
Even for SARIMA we have used 80:20 train test split for training the model.

### Observations
The graph plotted between predicted values and original values shows that they are almost similar to each other but with a gap between them. 