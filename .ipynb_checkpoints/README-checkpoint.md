# An exploratory data analysis to understand the real estate market in Edmonton.
### Introduction
For our money not to devalue due to inflation, we are told to invest. Unlike stocks investment where we could easily look for its performance over time, beside the cashflow, the performance of real estate market (appreciation) is not as publicly accessible. Being a highly analytical person, the lack of historical data to inform my investment decision in real estate market is troubling. As Gandhi has said that I must be the change I want to see in the world, in this post, we will utilize data science and the dataset provided by the City of Edmonton on historical property assessment to answer the following questions:
* Does residential or commercial real estate have higher Return on Investment (ROI)?
* What are top 3 most expensive neighborhoods for residential and commercial properties?
* How well can we predict a property's value? What aspects correlate well to the value of a property?
### How to run the notebook
To save you some time, I made the connection to the City of Edmonton's API and stored over 3 million rows of data in parquet folder. So in order to do exploratory data analysis on this dataset, you just need to establish the Spark connection and read from the parquet folder located in output/houses.parquet.