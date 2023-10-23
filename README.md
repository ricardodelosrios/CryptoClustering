# CryptoClustering

## Introduction

This repository contains a set of tools and code in Python designed to analyze and cluster cryptocurrency market data using clustering and principal component analysis (PCA) techniques. The main purpose of this project is to provide investors and analysts with a tool that allows them to understand and categorize the behavior of different cryptocurrencies based on their historical price change percentages.

Cryptocurrencies are known for their volatility and diversity, and analyzing their behavior can often be overwhelming due to the large amount of data available.

## Libraries 

1. **Pandas (ps)**: The “pandas” library is widely used for data manipulation and analysis in Python. It is imported with the alias "pd" for ease of use. You can load, manipulate and analyze data sets using pandas.
2. **hvplot.pandas**: "hvplot" is an extension to the "HoloViews" library that allows you to create interactive visualizations from pandas DataFrames. Facilitates effective data visualization.
3. **KMeans**: it import the "KMeans" class from the "sklearn" library (scikit-learn). K-Means is a machine learning algorithm used for cluster analysis. You can use it to group data into groups based on similarities.
4. **PCA**: it import the "PCA" class from "sklearn". Principal component analysis (PCA) is a dimensionality reduction technique commonly used to visualize data and reduce its complexity.
5. **StandardScaler**: it import the "StandardScaler" class from "sklearn". This layer is used to normalize (scale) numerical features, which is important in many machine learning algorithms, including K-Means. Reduce size by
in the data set. Make sure these libraries are installed in your environment before running the code.

## How the Code Works

### 1. Data Preparation

* Import the necessary libraries, including pandas, hvplot, and scikit-learn modules.
* Load the market data from the "crypto_market_data.csv" file into a Pandas DataFrame.
* Generate summary statistics for the loaded data.

### 2. Data Normalization

* Use the StandardScaler() from scikit-learn to normalize selected columns of the data.
* Create a new DataFrame with the scaled data, including the coin identifiers.
* Set the coin identifier as the index of the DataFrame.

### 3. Finding the Optimal Number of Clusters

* Determine the optimal number of clusters (k) for K-Means using two methods: the original data and PCA data.
* For both methods, create a list of possible k-values (1 to 10) and calculate the inertia for each k-value, which helps identify the "elbow point."
* Create elbow plots to visually identify the optimal k-values for clustering.

### 4. Clustering Cryptocurrencies

#### Using the Original Data

* Initialize a K-Means model with the chosen k-value (e.g., 4).
* Fit the model to the scaled data.
* Predict the clusters and add the cluster labels to the DataFrame.
* Create a scatter plot showing the relationship between 24-hour and 7-day price change percentages, color-coded by cluster.

#### Using PCA Data

* Apply PCA to the scaled data, reducing it to three principal components.
* Initialize a K-Means model with the same k-value as used for the original data.
* Fit the model to the PCA data.
* Predict the clusters and add the cluster labels to the PCA DataFrame.
* Create a scatter plot showing the relationship between the first two principal components, color-coded by cluster.

### 5. Visualizing and Comparing the Results

* Create composite plots to visualize the elbow curves for both the original data and PCA data, allowing for a comparison.
* Create composite plots to visualize the clustering results for both the original data and PCA data, providing insights into the grouping of cryptocurrencies.

By following the steps outlined in this code, users can effectively cluster cryptocurrencies based on their price change patterns and visualize the results, making it easier to understand and analyze the cryptocurrency market.

## Conclusion

the code provides a structured approach to analyzing and clustering cryptocurrency market data. It enables users to explore, preprocess, cluster, and visualize data, ultimately helping them make data-driven decisions and gain a better understanding of the behavior of cryptocurrencies in the market.




