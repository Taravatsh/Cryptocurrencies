# Cryptocurrencies

## Overview of Project

The purpose of this project is to use unsupervised machine learning to determine what cryptocurreencies exist on the trading market and how they could be grouped to build a classification system for development of a new investment. Since there is no known output unsupervised machine learning is used. Furthermore, the data that we will be working with has to be processed before grouping the cryptocurrencies using the clustering algorithm. As a result of this, the following steps has to be performed for preparing the an analysis for clients who are preparing to get into the cryptocurrency markey:

- Preprocessing the Data for PCA.
- Reducing the Data for PCA.
- Clustering Cryptocurrencies using K-means.
- Visualizing Cryptocurrencies Results.


## Results

This section of the project focuses on the results achieved after processing the data to fit the machine learning model.

### Preprocessing the Data for PCA 

In this part of the project, the data on the cryptocurrencies that was retrieved as a csv file from [CryptoCompare]() was preprocessed by performing the following:

- Keeping the cryptocurrencies that were being traded.
- Dropping the **IsTrading** column.
- Removing the rows that have at least one null value.
- Keeping the coins that have been mined.

Figure below illustrates the **crypto_df** after performing the aforementioned preprocessing steps.

![Crypto DataFrame]()

Additionlly, the text features of the data were transformed into numerical data type using the **get_dummies()** method as depicted in the figure below.
![Transforming features]()

### Reducing Data Dimensions using PCA

In this section of the project, Principal Component Analysis (PCA) algorithm, was performed for reducing the number of dimensions to only three principal components to prevent overfitting the data as demonstarted in the figure below.

![Reducing Data Dimensions]()

### Clustering Cryptocurrencies using K-means

In this section of the project, knowledge of K-means algorithm was used for creating an elbow curve using **hvplot** for finding the best K value as illustrated in the plot below.

![Elbow Curve]()

Looking at the elbow curve, the k value of 3 was selected since that is the point where the vertical direction shifts to a strong horizontal direction. Hence, the KMeans algorithm was then initialized for making predictions of the K-clusters for the cryptocurrencies' data and a new clustered DataFrame was created as illustrated in the figure below.

![Clustered DataFrame]()

### Visualizing Cryptocurrencies Results

In this part of the project Plotly Express and **hvplot** was used for visualzing the distinct groups that corresponded to the three principal components created. Additionally, a table showing the tradabke cryptocurrencies was created using **hvplot.table()** as shown in the figure below.

![Tradable Cryptocurrencies]()

 The scatter plot is illustrated in the figure below.

![Scatter Plot]()

## Summary

In conclusion, cryptocurencies were grouped together using KMeans clustering algorithm after preprocessing the data to fit the unsupoervised machine learning model. Hence, creating an analysis for the clients who are looking forward to get into the cryptocurrency market.