# DBSCAN
DBSCAN or Density-Based Spatial Clustering of Applications with Noise is an algorithm that clusters data points based on their density. This sounds familiar to other algorithms but DBSCAN doesn't need to know the number of clusters. It itself identifies the clusters and can also deal with any outlying data points which are called noise.

DBSCAN does need two parameters: the radius of the neighborhood around a point as well as the minimum number of data points to be considered a neighborhood/cluster. Then DBSCAN takes this information and identifies core points from which it will expand clusters with noise being considered data points that are unreachable.

It is better of arbitrary shapes and can easily handle noise compared to K-Means which is better for well-defined spherical clusters with less or no noise.

# DBSCAN (Density-Based Spatial Clustering of Applications with Noise)

**DBSCAN** is a powerful unsupervised machine learning algorithm used for **clustering data based on density** rather than distance to a centroid. It is particularly useful when dealing with datasets that contain **clusters of arbitrary shape** and **noise or outliers**, making it more robust than traditional methods like K-Means.

Unlike K-Means, **DBSCAN does not require the user to specify the number of clusters (`k`)** beforehand. Instead, it determines clusters dynamically by identifying areas of high point density. It’s especially effective for datasets where clusters are not well separated or evenly sized.

---

## Parameters

- The radius defining the neighborhood around a point.
- The minimum number of points required to form a dense region (including the core point).

---

## How DBSCAN Works

1. **Visit Each Point**:
   - For each unvisited point, find all points within the specified radius.

2. **Check Density**:
   - If the number of nearby points ≥ specified number of minimum points, it’s a core point and a new cluster is created.

3. **Expand Cluster**:
   - Recursively add all density-reachable points to this cluster by visiting all neighbors of core points.

4. **Label Noise**:
   - Points that do not belong to any cluster are marked as noise or outliers.

---

## Advantages

- **No Need to Specify Number of Clusters**: DBSCAN automatically determines the number of clusters.
- **Handles Arbitrary Shapes**: Clusters do not need to be spherical.
- **Robust to Outliers**: It effectively identifies and excludes noise points.
- **Works Well with Real-World Data**: Especially when noise and varying density are present.

---

## Disadvantages

- **Parameter Sensitivity**: Performance depends heavily on the choice of parameters.
- **Varying Densities**: Struggles when clusters have significantly different densities.
- **High-Dimensional Data**: Distance metrics become less meaningful as dimensionality increases.

---

## Uses

- **Anomaly Detection**: Identifying unusual patterns or fraud.
- **Geospatial Clustering**: Grouping geographical locations (e.g., hotspots of activity).
- **Market Segmentation**: Clustering customers or users when the number of segments is unknown.
- **Social Network Analysis**: Discovering tightly connected communities.