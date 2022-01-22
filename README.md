# Cryptocurrency Clusters

## Background
 Used unsupervised learnings to analyzed cryptocurrencies that are on the trading market and determine whether they can be grouped to create a classification system.

* Used several clustering algorithms to explore whether the cryptocurrencies can be grouped together with other similar cryptocurrencies. 

## Data Source
The dataset was obtained from [CryptoCompare](https://min-api.cryptocompare.com/data/all/coinlist).

### Data Preparation

* Read `crypto_data.csv` into Pandas. 
* Discarded all cryptocurrencies that are not being traded. In other words, filtered for currencies that are currently being traded. 
* Droped the `IsTrading` column from the dataframe.

* Removed all rows that have at least one null value.

* Filtered for cryptocurrencies that have been mined. That is, the total coins mined should be greater than zero.

*  Delete the `CoinName` from the original dataframe as the coin names do not contribute to the analysis of the data.

* Used Pandas to create dummy variables. 

* Standardized the dataset so that columns that contain larger values do not unduly influence the outcome.

### Dimensionality Reduction

* As by Creating dummy variables above dramatically increased the number of features in the dataset. 
* Performed dimensionality reduction with PCA. Rather than specify the number of principal components, created a model that will preserve approximately 90% of the explained variance using `PCA(n_components=0.90)`.

* Next, further reduced the dataset dimensions with t-SNE and visually inspect the results. I
* Created a scatter plot of the t-SNE output. 

### Cluster Analysis with k-Means

* Created an elbow plot to identify the best number of clusters. Used a for-loop to determine the inertia for each `k` between 1 through 10. 

 
