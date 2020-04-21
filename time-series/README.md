
# Mod 4 Project :

In this preject we are going to work with time series in order to predict the future property values for the 5 top zipcodes of San Jose Metro area in California based on the price of previous years.

[Jupyternotebook](https://github.com/FarnazG/dsc-mod-4-project-v2-1-online-ds-ft-120919/blob/master/time-series/Project4_final_notebook.ipynb)

[Presentation_pdf](https://github.com/FarnazG/dsc-mod-4-project-v2-1-online-ds-ft-120919/blob/master/time-series/Project4_presentation.pdf)


# Project Breakdown

1. Imorting necessary libraries and load the dataset.

2. separate out the San Jose metro area from the rest of the dataset to work with.

3. check dataset for missing data, data types and placeholders.

4. convert different zipcodes mean values into monthly ordered time-series from 1996-04-01 to 2018-04-01.

5. check time series stationarity.

6. finding the best model parameters to work with.

7. modeling and validating the results.

8. predicting future property values using the model.



# Initial Data and its zipcode based time series:

* Initial wide format dataset:

![alt text](https://github.com/FarnazG/dsc-mod-4-project-v2-1-online-ds-ft-120919/blob/master/images/df_head.png)


* Long format San Jose metro area dataset extracted from the initial dataset:

![alt text](https://github.com/FarnazG/dsc-mod-4-project-v2-1-online-ds-ft-120919/blob/master/images/SanJose_Metro_df.png)


### The general trend of property values for different cities in San Jose metro area:

![alt text](https://github.com/FarnazG/dsc-mod-4-project-v2-1-online-ds-ft-120919/blob/master/images/Gtrend_SJMetro_Property_Value.png)


* Zipcode based time series:

![alt text](https://github.com/FarnazG/dsc-mod-4-project-v2-1-online-ds-ft-120919/blob/master/images/Zip_Timeseries.png)


### Time series stationarity:

* Visualizing Autocorrelation and Partial-Autocollerlation plots of time series

![alt text](https://github.com/FarnazG/dsc-mod-4-project-v2-1-online-ds-ft-120919/blob/master/images/Autocorrelation.png)
![alt text](https://github.com/FarnazG/dsc-mod-4-project-v2-1-online-ds-ft-120919/blob/master/images/Partial_Autocorrelation.png)




# The ARIMA model initial result:

* In-sample predictions for test data:

![alt text](https://github.com/FarnazG/dsc-mod-4-project-v2-1-online-ds-ft-120919/blob/master/images/Timeseries_initial_model_result.png)


* Out_of_sample predictions for future years, from 2018 to 2020: 

![alt text](https://github.com/FarnazG/dsc-mod-4-project-v2-1-online-ds-ft-120919/blob/master/images/Timeseries_outofsample_model_result.png)


### Model validation using residuals and density plots:

![alt text](https://github.com/FarnazG/dsc-mod-4-project-v2-1-online-ds-ft-120919/blob/master/images/Model_validation.png)




# Interpreting Results:

### Finding best zipcodes within san jose metro area:

The prices are predicted for the next 2 years of our data set, from 2018 to 2020.To find the 5 top most growing zipcodes:

Calculate the percentage of profit made from the investment within 4 years from 2016 to 2020:

profit = (Predicted property value on 2020 – investment value on 2016)/investment value on 2016


![alt text](https://github.com/FarnazG/dsc-mod-4-project-v2-1-online-ds-ft-120919/blob/master/images/Five_top_zipcode.png)


* The most profitable and highest return of investment goes to zipcode 95050, Santa Clara:

![alt text](https://github.com/FarnazG/dsc-mod-4-project-v2-1-online-ds-ft-120919/blob/master/images/zip_95050.png)


* The second top profitable zipcode for investment is 94089, Sunnyvale

![alt text](https://github.com/FarnazG/dsc-mod-4-project-v2-1-online-ds-ft-120919/blob/master/images/zip_94089.png)


* Another 3 top ranked profitable zipcodes for investment are located in San Jose, 95131, 95130 and 95112.

* Zipcode 95112:

![alt text](https://github.com/FarnazG/dsc-mod-4-project-v2-1-online-ds-ft-120919/blob/master/images/zip_95112.png)


### Future work and recommendations:

Based on the data provided by zillow dataset, The generated ARIMA model is capable of predicting the average property value and its changes for any given period of time using the trends of previous years from 1996 to 2018.

For more accuracy, it seems better to keep short steps/periods of future predictions, longer periods of predictions will be more accurate after applying latest updates and changes to the dataset. 
