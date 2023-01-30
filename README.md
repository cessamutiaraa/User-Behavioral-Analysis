# Summary
This project was a group final project of Data Analytics Boot Camp which focused on how to increase Uber's order growth in 2015 by creating campaign suggestion using cluster analysis.
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
In order to find any trends or patterns, we did Exploratory Data Analysis (EDA) using Google Colaboratory which consist of analysis based on the distance, based on the time, based on month & days of the orders.
## Data Analysis & Visualization
### Customer Segmentation
To segment the users, we used cluster analysis using Elbow Method and Silhouette Analysis. The variables we included in the analysis are total fare, number of passangers, distance, and days of the orders.
For the categorical variables, we applied one-hot encoding to the data in order to convert it to numerical data. Thus, we can do the cluster analysis.
![image](https://user-images.githubusercontent.com/123222363/215429905-09b156e3-70e2-4d2c-b406-05824e13fa29.png)
