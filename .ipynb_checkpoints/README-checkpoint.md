# An exploratory data analysis to understand the real estate market in Edmonton.
### Introduction
For our money not to devalue due to inflation, we are told to invest. Unlike stocks investment where we could easily look for its performance over time, beside the cashflow, the performance of real estate market (appreciation) is not as publicly accessible. Being a highly analytical person, the lack of historical data to inform my investment decision in real estate market is troubling. As Gandhi has said that I must be the change I want to see in the world, in this post, we will utilize data science and the dataset provided by the City of Edmonton on historical property assessment to answer the following questions:
* Does residential or commercial real estate have higher Return on Investment (ROI)?
* What are top 3 most expensive neighborhoods for residential and commercial properties?
* How well can we predict a property's value? What aspects correlate well to the value of a property?
### Installation
If you would like to connect to the API yourself, please refer to the documentation here: https://data.edmonton.ca/City-Administration/Property-Assessment-Data-Historical-/qi6a-xuwt
### File Description
To save you some time, I made the connection to the City of Edmonton's API and stored over 3 million rows of data in parquet folder. So in order to do exploratory data analysis on this dataset, you just need to establish the Spark connection and read from the parquet folder located in output/houses.parquet.
### Summary of Results

Between 2012 and 2020, in addition to the cashflow from rental income, return on investment from property appreciation on multi-family and single-family properties are 58.60% and 5.46% respectively. In particular, if you bought an apartment building in 2012 for 1 million dollar, in 2020, your building would have appreciated to 1 million and a half dollar.
![plot](./bar_plot_ROI_by_property_type.png)

Although Multi Family real estate investment provides significantly higher ROI, it is much riskier than Single Family. While Single Family properties did not seem to fluctuate much from 2012 to 2020, Multi Family properties experienced a sharp decline between 2016 and 2017, but finally recovered and provided a substantial increase in 2020. Therefore, your risk tolerance would be a big factor in deciding whether to invest in single family or multi family properties.
![plot](./line_chart_by_property_type.png)

The Root Mean Squared Error of the trained model using the following features: property_type (Single family vs Multi family), lot_size, garage (Y/N), street_name, year_built, zoning, and type to determine assessed_value is 3,949,000 which is unacceptable. Although the model does not provide a great root mean squared error, it indicates that features such as zone, year_built, lot_size, and property_type (multi family vs single family) do significantly impact the value of a property. 
![plot](./feature_importance.png)
