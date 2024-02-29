# CryptoClustering

### Functionality Involved:

 > Prepare the Data
- Use the `StandardScaler()` module from scikit-learn to normalize the data from the CSV file
- Create a list with the number of k-values to try And use a range from 1 to 11
- Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.

**Question:** What is the best value for `k`?
- Answer: 3

 > Cluster Cryptocurrencies with K-means Using the Original Scaled Data.
- Fit the K-Means model using the scaled data
- Predict the clusters to group the cryptocurrencies using the scaled data
- Create a copy of the DataFrame.
- Create a scatter plot using Pandas plot by setting x=price_change_percentage_24h and y=price_change_percentage_7d. 

 > Optimize Clusters with Principal Component Analysis.
- Fit the K-Means model using the scaled data
- Use the PCA model with `fit_transform` on the original scaled DataFrame to reduce to three principal components.
- Retrieve the explained variance to determine how much information  can be attributed to each principal component.

- **Question:** What is the total explained variance of the three principal components?

- Answer: About 88% of the total variance is condensed into the 3 PCA variables.

 > Find the Best Value for k Using the PCA Data
 - Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.
 - **Question:** What is the best value for `k` when using the PCA data?

- Answer: 4

- **Question:** Does it differ from the best k value found using the original data?

- Answer: Yes

 > Cluster Cryptocurrencies with K-means Using the PCA Data.
 - Create a scatter plot using hvPlot by setting `x="PCA1"` and `y="PCA2"`. 
 
 > Determine the Weights of Each Feature on each Principal Component

 - Question: Which features have the strongest positive or negative influence on each component? 
 
- Observation: 
- "price_change_percentage_200d", "price_change_percentage_1y" have the strongest positive influence on PCA1. 
- "price_change_percentage_14d" and "price_change_percentage_30d" have the strongest positive influence on PCA2
- "price_change_percentage_7d" has the strongest positive influence on PCA3.   

