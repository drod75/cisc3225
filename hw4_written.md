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

2. Regardless of your answer above, would missing values be a problem for clustering? Why or why not?

3. Which columns contain continuous values? For these columns, use describe() to show basic summary

4. Which columns contain categorical values? Use value counts() to show the unique values contained
in each column, and how often they appear.

5. Of the categorical columns, which contain binary yes/no values? What do the yes/no values mean?



## 2 Preprocessing (6 points)
Perform any steps necessary to preprocess the dataset to prepare it for clustering. This could include one-hot
encoding, producing binary 0/1 values, or standardizing with Z-score normalization.

Please note that, if you want to perform one-hot encoding on the “year” column, you must transform it
to a string first: df['year'] = df['year'].astype(str)



## 3 K=2 (8 points)
Perform K-means clustering with K=2 (3 points). Answer the following questions:

1. (1 point) How many rows are in each cluster?

2. (4 points) Average all columns within each cluster. Using these averages, find a cluster with the least
bike rentals and a cluster with the most bike rentals, then describe them. Why do you think fewer
people are renting bikes in the least-rented cluster?



## 4 K=3 (10 points)
Perform K-means clustering with K=3 (3 points). Answer the following questions:

1. (1 point) How many rows are in each cluster?

2. (4 points) Average all columns within each cluster. Using these averages, find a cluster with the least
bike rentals and a cluster with the most bike rentals, then describe them. Why do you think fewer
people are renting bikes in the least-rented cluster?

3. (2 points) Based on what you’ve seen so far, which value of K (K=2 or K=3) provides more useful
insight into bike rental patterns? Why?



## 5 Elbow Method (11 points)
Use the elbow method with inertia scores to approximate an ideal value of K. Once you have done this,
perform a K-means clustering with this value of K you discovered (6 points). Answer the following questions:

1. (1 point) How many rows are in each cluster?

2. (4 points) Average all columns within each cluster. Using these averages, find a cluster with the least
bike rentals and a cluster with the most bike rentals, then describe them. Why do you think fewer
people are renting bikes in the least-rented cluster?
