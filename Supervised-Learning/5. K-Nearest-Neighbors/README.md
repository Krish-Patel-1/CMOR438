# K Nearest Neighbors (KNN)

**K Nearest Neighbors (KNN)** is a simple, intuitive, and powerful **supervised machine learning algorithm** used for both **classification** and **regression** tasks. It is a **non-parametric** method, meaning it makes no underlying assumptions about the distribution of the data. Instead, it relies entirely on the structure of the data itself to make predictions.

The key assumption behind KNN is that **similar data points exist close to each other in the feature space**. In other words, "birds of a feather flock together"—so if you want to classify a new data point, look at how its **nearest neighbors** are classified and make a decision based on that.

---

## How KNN Works

The KNN algorithm works in the following steps:

1. **Choose a value for K**, the number of nearest neighbors to consider.
2. **Calculate the distance** (typically using Euclidean distance) between the new data point and all other data points in the training set.
3. **Sort the distances** and select the K closest data points.
4. **Vote or average** the values of these neighbors:
   - For **classification**, use **majority vote** (the most common label among the K neighbors).
   - For **regression**, take the **average** of the K neighbors' values.
5. Return the predicted label or value based on the result.

For example, if `K = 5`, and 3 of the 5 closest neighbors are labeled "cat" and 2 are labeled "dog", then the new point will be classified as "cat".

---

## Choosing the Right K

Choosing an appropriate value for **K** is crucial:

- A **small K** (e.g., K = 1) can be very sensitive to noise and outliers.
- A **large K** can smooth out the predictions but might include points from other classes, leading to misclassification.
- A good rule of thumb is to try several values and use **cross-validation** to find the K that yields the best accuracy on validation data.

---

## Distance Metrics

The effectiveness of KNN depends on the distance metric used to measure closeness between points. Common metrics include:

- **Euclidean Distance**: 
  \[
  d(p, q) = \sqrt{(p_1 - q_1)^2 + (p_2 - q_2)^2 + \cdots + (p_n - q_n)^2}
  \]
- **Manhattan Distance**: 
  \[
  d(p, q) = |p_1 - q_1| + |p_2 - q_2| + \cdots + |p_n - q_n|
  \]
- **Minkowski Distance**: A generalization of both Euclidean and Manhattan distances.

The choice of metric can affect the performance and behavior of the KNN algorithm.

---

## Advantages

- **Simple and Easy to Implement**
- **No Training Phase**
- **Naturally Adapts** to multi-class classification.
- **Works Well with Small Datasets** with clearly defined boundaries.

---

## Disadvantages

- **Computationally Expensive**: Requires calculating distances to all training points at prediction time.
- **Sensitive to Irrelevant Features**: All features are treated equally unless data is preprocessed.
- **Poor Performance on High-Dimensional Data** due to the "curse of dimensionality."
- **Does Not Scale Well**: Slower as dataset size increases.

---

## Applications

KNN is used in various real-world scenarios such as:

- **Recommender systems** (e.g., suggesting movies or products based on similar users)
- **Medical diagnostics** (e.g., predicting disease presence from patient data)
- **Pattern recognition** (e.g., handwriting, image classification)
- **Anomaly detection** (e.g., fraud detection)