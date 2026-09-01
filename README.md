# Data Science Project - Using an ARIMA Model to predict Audience Attendance to the musical "Miss Saigon"

## In this project I have used an ARIMA Time Series Model to predict future audience attendance to the Broadway show "Miss Saigon".

### Musical Theatre relies on audience attendance to keep shows running and financially viable, being able to predict audience attendance allows shows to determine viability of extending runs, maximise ticket pricing and sales, as well as assess potential deteriorations in audience attendance allowing for interventions to be made early.

### This project uses a dataset from Kaggle called Broadway, which can be downloaded from: https://www.kaggle.com/datasets/mexwell/broadway-shows. This data set requires engineering in order for it to be used in the model sufficiently due to missing dates and data inconsistencies.

### I have used Excel Power Query to engineer the data before then completing full Exploratory Data Analysis (EDA) and an ARIMA Model within Python. Excel Power Query was chosen over Python to complete the data wrangling due to the ease of use (being no code), the size of the data and due to the types of engineering required being relatively straightforward in Excel where they may be less straightforward in Python.

### I have completed Autocorrelation (ACF) and Partial Autocorrelation (PACF), the ACF indicates shows a positive correlation between the time series and the lagged version of itself, as the lags increase however all lags sit outside of the significance. The PACF shows the lags once the effects of shorter lags have been removed, this is helpful for determining the best order for ARIMA.

![ACF & PACF Graphs](https://github.com/DataSage26/Data-Science-Project---Attendance-Time-Series-Analysis/blob/main/ACF%20%26%20PACF.png)

### I evaluated the parameters of various p, d and q values to determine the order for the ARIMA where it was determined that 10, 0, 1 provided the best based on the train dataset, this gave a RMSE of 1072.091 which indicates the model is going to have a significant error margin. 

### The Results of the model show that the model was not effective at predicting audience attendance compared to the actual data. 
