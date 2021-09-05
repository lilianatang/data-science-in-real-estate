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
