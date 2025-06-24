# DBSCAN
DBSCAN or Density-Based Spatial Clustering of Applications with Noise is an algorithm that clusters data points based on their density. This sounds familiar to other algorithms but DBSCAN doesn't need to know the number of clusters. It itself identifies the clusters and can also deal with any outlying data points which are called noise.

DBSCAN does need two parameters: the radius of the neighborhood around a point as well as the minimum number of data points to be considered a neighborhood/cluster. Then DBSCAN takes this information and identifies core points from which it will expand clusters with noise being considered data points that are unreachable.

It is better of arbitrary shapes and can easily handle noise compared to K-Means which is better for well-defined spherical clusters with less or no noise.