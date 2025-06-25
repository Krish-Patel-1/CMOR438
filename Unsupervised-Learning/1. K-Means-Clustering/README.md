# K-Means Clustering

**K-Means Clustering** is one of the most widely used unsupervised machine learning algorithms for **partitioning unlabeled data** into a specified number of clusters (`k`). The goal is to divide the data into `k` distinct, **non-overlapping clusters**, where each data point belongs to the cluster with the **nearest mean (centroid)**. It is particularly effective for large datasets where the underlying groupings are not known in advance.

---

## Key Concepts

- **Clusters**: Groups of similar data points.
- **Centroid**: The center of a cluster; calculated as the mean position of all the points in that cluster.
- **K**: The number of clusters to form; this must be specified before training begins.
- **Distance Metric**: Typically uses Euclidean distance to determine the closest centroid for each data point.

---

## How K-Means Works

1. **Initialization**:
   - Randomly choose `k` initial centroids.

2. **Assignment Step**:
   - Assign each data point to the nearest centroid based on the chosen distance metric.

3. **Update Step**:
   - Recalculate the centroids by finding the mean of all data points assigned to each cluster.

4. **Repeat**

---

## Example

Assume `k = 3`:
- The algorithm will attempt to find 3 distinct clusters in the data.
- Each point will be assigned to one of the 3 centroids.
- The centroids will shift their position based on the updated cluster members after each iteration.

---

## Advantages

- **Simplicity and Speed**: Easy to understand and implement. Computationally efficient, especially with large datasets.
- **Scalability**: Works well with large amounts of data.
- **Efficiency**: Fast convergence in most practical situations.

---

## Disadvantages

- **Must Specify K**: You must predefine the number of clusters (`k`), which may not always be obvious.
- **Sensitive to Initialization**: Poor initial centroid placement can lead to suboptimal clustering.
- **Assumes Spherical Clusters**: Performs poorly on non-globular clusters or clusters of different densities and sizes.
- **Hard Assignment**: Each point is assigned to exactly one cluster (not probabilistic), which may not reflect real-world ambiguity.

---

## Choosing the Right K

One of the challenges in using K-Means is determining the optimal number of clusters. Common methods include:

- **Elbow Method**: Plot the total within-cluster sum of squares (WCSS) against the number of clusters. The "elbow" point suggests the optimal `k`.
- **Silhouette Score**: Measures how similar a data point is to its own cluster compared to other clusters.

---

## Real-World Applications

- **Customer Segmentation**: Grouping customers by purchasing behavior.
- **Market Basket Analysis**: Finding related product groups.
- **Image Compression**: Reducing the number of colors in an image by grouping similar pixel values.
- **Document Categorization**: Automatically clustering news articles or research papers.