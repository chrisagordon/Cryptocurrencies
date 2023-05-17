# Unsupervised Machine Learning Clustering of Market Cryptocurrencies
## Using PCA and k-means algorithm

## 1. OVERVIEW
Cryptocurrency data is given and a client is asking for the data to be grouped into classifications to further understand their investment value. The data is large and has many identifying characteristics for each Coin Name such as: Algorithm, IsTrading, ProofType, TotalCoinsMined and TotalCoinSupply. Using PCA to reduce the number of components to 3 and k-means we were able to cluster our cryptocurrencies into 4 different categories and place these into a tradable dataframe that was visualized using 3-D and 2-D Scatterplots.  

## 2. RESULTS
### Data Cleasing
Below is an image of our Raw Dataframe when imported into Jupyter Notebook 
![This is an image](https://github.com/chrisagordon/Cryptocurrencies/blob/main/Challenge/Images/Raw%20Dataframe.PNG)

By removing the untraded cryptocurrencies, rows with null values, coins that aren't being mined, and coins without a name we were able to clean excess data starting at 1252 rows down to 532 rows. See the dataframe below: 
![This is an image](https://github.com/chrisagordon/Cryptocurrencies/blob/main/Challenge/Images/Final%20Dataframe%20Cryptocurrencies.PNG) 

### Data Categorization

Next, using get dummies and standardizing the data by scaling it into 5 arrays we were able to produce these dataframes 

![This is an image](https://github.com/chrisagordon/Cryptocurrencies/blob/main/Challenge/Images/Using%20GetDummies%20on%20Dataframe.PNG) 
![This is an image](https://github.com/chrisagordon/Cryptocurrencies/blob/main/Challenge/Images/Standard%20Scaling%20Dataframe.PNG)

From there, using PCA the coins features were reduces into three separate values and an elbow curve was created using the inertia and number of k values to determine the correct number of clusters for a k-means model 
![This is an image](https://github.com/chrisagordon/Cryptocurrencies/blob/main/Challenge/Images/K%20value%20curve%20graph.PNG)

The k-means model was ran and the coins were sorted into 4 categories here is the 3-D Scatterplot generated 
![This is an image](https://github.com/chrisagordon/Cryptocurrencies/blob/main/Challenge/Images/3-D%20Scatterplot.PNG)

We also created a 2-D Scatterplot using the Total Coins Mined against the Total Coin Supply 
![This is an image](https://github.com/chrisagordon/Cryptocurrencies/blob/main/Challenge/Images/Scatter%20of%20Coins%20Mined%20vs%20Supply.PNG)



## 3. SUMMARY
- Using PCA and K-means we have taken dat from 1252 Cryptocurrencies to 532 tradable ones. These can be seen in the dataframe below. However the client would like to use this infromation to recommend investments is up to them.
![This is an image](https://github.com/chrisagordon/Cryptocurrencies/blob/main/Challenge/Images/Tradeable%20Cryptocurrencies%20Dataframe.PNG)
- Additionally the 2-D scatterplot comparing Total Coins Mined against the Total Coin Supply may be an indicator of coin usage and movement which could drive investments, seeing where group 0 clustered coins are concentrated in the bottom left of the graph may indicate they are traded and mined often and would be an interesting market investment.

