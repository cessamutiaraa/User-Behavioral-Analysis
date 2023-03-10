# Summary
This project was a group final project of Data Analytics Boot Camp which focused on how to increase Uber's order growth in 2015 by creating campaign suggestions using cluster analysis.
The dataset contains Uber Inc's order data in New York City from January 2009 - June 2015. We found that orders were having a downward trend from 2012, and from that trend, we aimed to increase the orders by creating customer segmentation using K-means clustering analysis (Silhouette & Elbow Method), and to reduce the dimensionality of the dataset we used Principal Component Analysis (PCA) for better interpretation & visualization. On top of that, we created the suggested campaign for each customer segmentation, and also created the prediction of the order increase using Timeseries-Analysis Prophet if Uber manages to execute the campaigns successfully. Finally, we created a dashboard for reporting each metric and important variable using Tableau.
# Dataset
The Dataset used was Uber Inc Order's data in New York City from January 2009 to June 2015 (200,000 orders/transactions)

Data Features consist of order id, fare of each trip, pickup datetime, passenger count, and coordinates of pickup and drop off location.
# Project Goals
How to increase Uber’s order growth by 3% within a year from 2014?

![image](https://user-images.githubusercontent.com/123222363/216353887-049d0b4a-8563-4150-a977-1509e0a9b92e.png)


For the project purpose, 2015 would become the year that Uber should implement the suggested campaign, since we only had the data from January - June, the campaign focused on how to increase the orders in July - December, so Uber could increase ~ 3% of the total orders in 2015
# Methodology
## Data Preparation & Cleaning
Data Preparation, Outlier and Null Cleaning are fully done with Python (Google Colaboratory).
In order to find any trends or patterns, we did Exploratory Data Analysis (EDA) using Google Colaboratory which consist of analysis based on the distance, based on the time, based on month & days of the orders.
## Data Analysis & Visualization
### Customer Segmentation
To segment the users, we used K-means clustering using Elbow Method and Silhouette Analysis. The variables we included in the analysis are total fare, number of passangers, distance, and days of the orders.
For the categorical variables, we applied one-hot encoding to the data in order to convert it to numerical data. Thus, we can do clustering analysis.
- Elbow Method
 ![image](https://user-images.githubusercontent.com/123222363/215431675-6216a5bf-8057-4f01-a1fd-49654ee6905e.png)

- Silhouette Analysis

 ![image](https://user-images.githubusercontent.com/123222363/215431596-3b2b8f3a-a8de-4106-94fd-8da76d0a184d.png)

And to reduce the dimensionality of the dataset we used Principal Component Analysis (PCA) for better interpretation & visualization, as shown in the graphic below

![image](https://user-images.githubusercontent.com/123222363/215432363-06977188-c8df-4fda-9b7b-3aa49ab45dda.png)

From above analysis, we could say that the users could be divided into 8 clusters that we could summarize it based on the variable that distinguised them, i.e day category (weekdays and weekend)

![image](https://user-images.githubusercontent.com/123222363/215432845-cda7d495-7aca-4276-a8dd-b3c8abd84b95.png)

### Campaign Suggestion
Since the cluster was considered too many to be applied campaign suggestion, We analyzed some variables that we could find the simmilarity among the 8 clusters:
1. The day category of the trips
Total trips in each cluster shows that uber is dominated by user who like to go trips in weekdays (typically it is routine activities).

![image](https://user-images.githubusercontent.com/123222363/216354235-8d0edf24-23be-4ab6-8733-03ba63e1c71b.png)

2. The peak hours of each day category

The peak hours in weekdays

![image](https://user-images.githubusercontent.com/123222363/216355804-85df7ced-d656-4eb0-8557-d9a77828e767.png)

The peak hours in weekend

![image](https://user-images.githubusercontent.com/123222363/216354565-b76bae9c-8503-41be-95ce-3b1769ccb8fe.png)

3. Average order value (AOV)
All clusters have the same average trip value (~USD 10), except for cluster 4 & 5 which have slightly higher value than the others.

![image](https://user-images.githubusercontent.com/123222363/216354660-00d4dc10-e902-495d-9899-cf009cdfdd1d.png)


4. The average of distance
All cluster have the same distance level (near level <= 5 KM) and the average is ~3 KM, except for cluster 4 & 5.

![image](https://user-images.githubusercontent.com/123222363/216354729-f22cfcb1-9526-476f-8e51-b1272750c57c.png)


5. The average of passenger
All clusters have the same average of total passenger (~2). This is correlated with the type of uber that user might be ordered.

![image](https://user-images.githubusercontent.com/123222363/216354889-703f116d-31ad-4f18-a96a-f3deba28b653.png)


We could narrowed the cluster into 3 groups for the campaign suggestion purposes based on above analysis,

![image](https://user-images.githubusercontent.com/123222363/216217409-b2bed330-ea25-4e74-81c3-c2a8cabea5f0.png)

Here, the suggested campaign based on the cluster grouping above,

![image](https://user-images.githubusercontent.com/123222363/216218029-70625183-b500-488e-addc-059ea6308e4e.png)


### Dashboard
We also created a dashboard of this project with Tableau https://public.tableau.com/app/profile/cessa.mutiara.aziz/viz/shared/BYS6Z2QZQ

<img width="387" alt="image" src="https://user-images.githubusercontent.com/123222363/217935121-44890791-27ba-4c80-81ef-4d70a026997d.png">


## Forecasting Analysis - Expected Outcome
For the expected outcome of the suggested campaign, we used forecasting analysis with Prophet method since it works best with time series that have strong seasonal effects and several seasons of historical data. Also it is robust to missing data and shifts in the trend, and typically handles outliers well.

As we know, since the trend has down trend, so it does the forecasting for the some times in the future as shown in the graph belows:

![image](https://user-images.githubusercontent.com/123222363/216220139-3d7dc088-59b7-4d0c-b0c7-4051dd59b5df.png)

Thus, to create an expected outcome if Uber can successfully implement the campaign, we decided to create a new data that the number of orders has been increased by 35% in the 2nd Semester of 2015 (from the result of the forecasting) to give a total increase ~ 3% in 1 year (2015).

![image](https://user-images.githubusercontent.com/123222363/216225284-92ce9e8d-7235-41e3-87d5-18682dee58a8.png)

## Further Analysis
The analysis can be more comprehensive if we have revenue and cost data to do profit analysis and we can do a more detail & targeted of customer segmentation analysis if we can access more information of the users.
