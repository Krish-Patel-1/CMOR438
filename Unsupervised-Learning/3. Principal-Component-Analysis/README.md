# Principal Component Analysis (PCA)
PCA's main job is dimensionality reduction. This the algorithm reducing the number of features by projecting data onto principal component that maximize variance. Only significant data is kept for further analysis.

The first principal component is a direction that maximizes variance of the data. The second principal component is the next component that maximizes variance and is orthogonal to the first principal component.

PCA transforms data into a lower-dimensional space and can be used for visualizing high-dimensional data more easily and preprocessing for other machine learning models such as DBSCAN.