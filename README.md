# Module 11 Challenge: CryptoClustering
## Problem Statement

Find clusters among 41 different Crypto currencies whose price fluctuation are given on timescales of 24 hours, 7 days, 14 days, 30 days, 60 days, 200 days, and 1 year.

## Solution
Using the KMeans algorithm, clusters are identified using the original data and after applying Principal Component Analysis (PCA) to reduce the dimensionality of the original data. The clusters resulting using the original data and after applying PCA are plotted and compared visually.

### Implementation
1. Import the data.
2. Prepare the data by normalizing all columns.
3. Find the best value of `k` (number of data clusters) by applying the Elbow Method on the original scaled data. We find that the Elbow Method suggests that `k=4` is the best value.
4. Apply the KMeans model to separate each crypto currency into one of the four clusters,
5. Use a scatter plot to visualize the clusters.
6. Use PCA to reduce the dimensionality of the data from 7 to 3.
7. Calculate the variance of the original data that is captured by the three principal components.
8. Use the Elbow Method on the PCA data to find the best value for `k`. It turns out that `k=4` is again the best value.
9. Apply the KMeans model to separate the PCA data into clusters.
10. Use a scatter plot to visualize the PCA clusters and realize that they look very similar to the original clusters.
11. Calculate the weights that each fluctuation timescale has on each principal component.

## Results
Using the elbow method on the original data and after PCA was applied, we find that both methods yield the same best value of four for the number of data clusters.

We further find that using three principal components captures 89.5% of the variance of the original system whereas using only two principal components captures only 71.9% of the variance in the data. We therefore use three principal components.

Visually comparing the clusters produced using the original data with the clusters produced after PCA shows that they are very similar, justifying the reduction of the dimensionality of the system from 7 to 3.

We finally find that the different principal components capture the variances of different combinations of timescales.