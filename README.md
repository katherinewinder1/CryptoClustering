# CryptoClustering
# Prepared the Data
Used the StandardScaler() module from scikit-learn to normalize the data from the CSV file.

Created a DataFrame with the scaled data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

# Find the Best Value for k Using the Original Scaled DataFrame
Used the elbow method to find the best value for k using the following steps:

Create a list with the number of k values from 1 to 11.
Create an empty list to store the inertia values.
Create a for loop to compute the inertia with each possible value of k.
Create a dictionary with the data to plot the elbow curve.
Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.

# Cluster Cryptocurrencies with K-means Using the Original Scaled Data
Use the following steps to cluster the cryptocurrencies for the best value for k on the original scaled data:

# Initialize the K-means model with the best value for k.
Fit the K-means model using the original scaled DataFrame.
Predict the clusters to group the cryptocurrencies using the original scaled DataFrame.
Create a copy of the original data and add a new column with the predicted clusters.
Create a scatter plot using hvPlot

# Optimize Clusters with Principal Component Analysis
Using the original scaled DataFrame, perform a PCA and reduce the features to three principal components.

Retrieve the explained variance to determine how much information can be attributed to each principal component and then answer the following question in your notebook:

The total explained variance of the three principal components: About 88%

Create a new DataFrame with the PCA data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

# Find the Best Value for k Using the PCA Data
Use the elbow method on the PCA data to find the best value for k using the following steps:

Create a list with the number of k-values from 1 to 11.
Create an empty list to store the inertia values.
Create a for loop to compute the inertia with each possible value of k.
Create a dictionary with the data to plot the Elbow curve.
Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.

The best value for k when using the PCA data is 4. This does not differ from the best k value found using the original data.

#Cluster Cryptocurrencies with K-means Using the PCA Data
Cluster the cryptocurrencies for the best value for k on the PCA data by:

Initializing the K-means model with the best value for k.
Fit the K-means model using the PCA data.
Predict the clusters to group the cryptocurrencies using the PCA data.
Create a copy of the DataFrame with the PCA data and add a new column to store the predicted clusters.
Create a scatter plot using hvPlot
