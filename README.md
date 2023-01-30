# Summary
This project focused on how to increase Uber's order growth in 2015 by creating campaign suggestion using cluster analysis.
The dataset contains Uber Inc's order data in New York City from January 2009 - June 2015.
We found that orders were having down trend from 2012, and from that trend we aimed to increase the orders by creating customer segmentation using cluster analysis (Silhouette & Elbow Method) and to reduce the dimensionality of the dataset we used Principal Component Analysis (PCA) for better interpretation & visualization. On top of that, we created the suggested campaign to each customer segmentation, also created the prediction of the order increase using Timeseries-Analysis Prophet if Uber manages to execute the campaigns successfully. FInally, we created a dashboard for reporting of each metrics and important variables using Tableau
# Dataset
The Dataset used was Uber Inc Order's data in New York City from January 2009 to June 2015 (200,000 orders/transactions)
Data Features consist of order id, fare of each trip, pickup datetime, passenger count, and coordinates of pickup and drop off location.
# Project Goals
How to increase Uber’s order growth by 3% within a year from 2014?
# Methodology
## Data Preparation & Cleaning
Data Preparation, Outlier and Null Cleaning are fully done with Python (Google Colaboratory).
In order to find any trends or patterns, , we also use Colab for E
