# Homework 4
45 points
Due Thursday, April 10 at 11:59 PM

For this assignment, you will investigate patterns of bicycle rentals using K-means clustering with this
dataset: https://raw.githubusercontent.com/CUNY-CISC-3225/datasets/main/bike_rentals.csv.
The dataset contains data from 2 years of bicycle rental data. Each row represents a single rental period,
which consists of an hour. The columns give information about the rental period including the season,
weather, and what kind of day it is (working day and holiday). It also includes a “count” column, which
indicates the number of bikes rented over the hour. Note that the “temp” column contains the actual
temperature in Celsius, and “atemp” contains an estimate of the sensation of temperature in Celsius.
The purpose of this investigation is to characterize different types of rental periods based on how many
people are renting bikes. In other words, when are many people renting bikes, and when are few people
renting bikes?

## 1 Analysis (10 points)
Perform a basic exploratory analysis of the dataset. The goal of this analysis should be to identify whether
each column is continuous or categorical.
1. Are there any missing values?
    There are no missing values, all columns contain 7689 entries which is the length of the dataframe.

2. Regardless of your answer above, would missing values be a problem for clustering? Why or why not?
    Missing values would be a problem for clustering because that would mean the data is missing key values that could be used to cluster the data.

3. Which columns contain continuous values? For these columns, use describe() to show basic summary
    The columns that contain continuous data are: year, hour, workingday, temp, atemp, humidity, windspeed, count

4. Which columns contain categorical values? Use value counts() to show the unique values contained
in each column, and how often they appear.
    The columns that contain categorical data are: season, holiday, and weather

5. Of the categorical columns, which contain binary yes/no values? What do the yes/no values mean?
    The column that has binary data is workingday, 1 means yes its a working day, 0 means no its not


## 2 Preprocessing (6 points)
Perform any steps necessary to preprocess the dataset to prepare it for clustering. This could include one-hot
encoding, producing binary 0/1 values, or standardizing with Z-score normalization.

Please note that, if you want to perform one-hot encoding on the “year” column, you must transform it
to a string first: df['year'] = df['year'].astype(str)



## 3 K=2 (8 points)
Perform K-means clustering with K=2 (3 points). Answer the following questions:

1. (1 point) How many rows are in each cluster?
    There are 2 clusters with 4023 rows within cluster 1 and 3666 rows within cluster 0

2. (4 points) Average all columns within each cluster. Using these averages, find a cluster with the least
bike rentals and a cluster with the most bike rentals, then describe them. Why do you think fewer
people are renting bikes in the least-rented cluster?
    Based on the data it seems the cluster with the least rentals is cluster 1 with 108.74 and the cluster with the most is cluster 0 with 282.15, the reason for this could be that cluster one
    contains more winter, autumn, and humidity than cluster 0, this is typically considered more where colder weather comes out, and cold weather means more heavy clothing which is considered a nightmare for biking since combined with the sweating from biking it could be dangerous. While cluster 0 contains more spring and summer which means less clothes is a given, if you notice in the olympics bikers have thin and light clothes to help them stay regulated.


## 4 K=3 (10 points)
Perform K-means clustering with K=3 (3 points). Answer the following questions:

1. (1 point) How many rows are in each cluster?
    There are three clusters with 2662 rows within cluster 0, 2618 rows within cluster 1, and 2409 rows within cluster 2

2. (4 points) Average all columns within each cluster. Using these averages, find a cluster with the least
bike rentals and a cluster with the most bike rentals, then describe them. Why do you think fewer
people are renting bikes in the least-rented cluster?
    The cluster with the least amount of rentals is cluster 1 with a count of around 78.59, and the most is cluster 0 with a count of 349.23. The reason for this might be at a few columns, the most notable being humidity, autumn, winter, bad weather, and hour. In cluster 1 humidity and bad weather is more prominent and the hour is lower than the rest. This must show that because of the harsher conditions and lese time for ideal biking sales are down during these times, and the small hours of great biking conditions because of the worse weather around the time means biking is not ideal compared to the other clusters most prevalent conditions.

3. (2 points) Based on what you’ve seen so far, which value of K (K=2 or K=3) provides more useful
insight into bike rental patterns? Why?
    Given what we have seen so far the cluster amount, aka 2 or 3, with more useful info is with 2 clusters, the reason is with three there is not much of a difference besides smaller and harder patterns to make conclusive decisions on, with two clusters the data is much more usable and more patterns can be seen.



## 5 Elbow Method (11 points)
Use the elbow method with inertia scores to approximate an ideal value of K. Once you have done this,
perform a K-means clustering with this value of K you discovered (6 points). Answer the following questions:

1. (1 point) How many rows are in each cluster?
    Within each cluster there are: 
    for cluster 3 there are 1972 rows, 
    for cluster 1 there are 1451 rows, 
    for cluster 2 there are 1435 rows, 
    for cluster 4 there are 1432 rows, 
    and for cluster 0 there are 1399 rows

2. (4 points) Average all columns within each cluster. Using these averages, find a cluster with the least
bike rentals and a cluster with the most bike rentals, then describe them. Why do you think fewer
people are renting bikes in the least-rented cluster?
    The cluster with the least amount of sales is cluster 0, and with the most is cluster 3. The key reason may that be the average hour in cluster 0 is low, the temp is the lowest, its peretty humid, theres not that much wind, and theres more holidays than cluster 3. This could indicate that the average day within cluster 0 is worse leading to a not so ideal day for biking, this of course affects sales causing a drop in sales.
