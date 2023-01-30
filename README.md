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
For the categorical variables, we applied one-hot encoding to the data in order to convert it to numerical data. Thus, we can do clustering analysis.
- Elbow Method
 ![image](https://user-images.githubusercontent.com/123222363/215431675-6216a5bf-8057-4f01-a1fd-49654ee6905e.png)

- Silhouette Analysis
 ![image](https://user-images.githubusercontent.com/123222363/215431596-3b2b8f3a-a8de-4106-94fd-8da76d0a184d.png)

And to reduce the dimensionality of the dataset we used Principal Component Analysis (PCA) for better interpretation & visualization, as shown in the graphic below
![image](https://user-images.githubusercontent.com/123222363/215432363-06977188-c8df-4fda-9b7b-3aa49ab45dda.png)

From above analysis, we could say that the users could be divided into 8 cluster that we could summarize it based on the variable that distinguised them, i.e day category (weekdays and weekend)
![image](https://user-images.githubusercontent.com/123222363/215432845-cda7d495-7aca-4276-a8dd-b3c8abd84b95.png)
