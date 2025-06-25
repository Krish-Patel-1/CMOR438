# Decision and Regression Trees

**Decision Trees** and **Regression Trees** are popular supervised machine learning models that use a **tree-like structure** to make decisions or predictions based on input data. They are highly interpretable, easy to visualize, and useful for both classification and regression tasks.

---

## Structure of a Tree

A decision tree is organized in a hierarchical manner, consisting of the following components:

- **Root Node**: The starting point of the tree; represents the entire dataset. It contains no incoming edges and initiates the process of splitting based on the most significant feature.
- **Internal Nodes (Decision Nodes)**: Nodes where decisions are made based on input feature values. These nodes split the data into subsets by evaluating a condition (e.g., `feature ≤ threshold`).
- **Branches**: Paths that connect nodes and represent the outcome of a decision at a parent node.
- **Leaf Nodes (Terminal Nodes)**: The end-points of a tree. Each leaf node holds a prediction—either a class label (in classification trees) or a numeric value (in regression trees).

---

## Criteria for Splitting (Classification Trees)

For classification tasks, decision trees use the following metrics to evaluate the quality of a split:

- **Gini Impurity**: Measures how often a randomly chosen element would be incorrectly labeled.
- **Entropy / Information Gain**: Measures the purity of a dataset before and after a split; the goal is to maximize the information gained from each split.

---

## Regression Trees

Regression trees are similar to decision trees but are used when the target variable is **continuous** instead of categorical. In this case:

- Splits are chosen to **minimize the variance** (or Mean Squared Error) in the target variable within each node.
- Leaf nodes contain a **numerical value**, typically the **average** of the output values of the data points within that node.
- The goal is to ensure that each subset (node) is as **homogeneous** as possible in terms of the target value.

---

## Advantages

- **Easy to Understand and Interpret**: Decision trees are one of the most transparent machine learning models.
- **No Need for Feature Scaling**: Works well with both numerical and categorical features without normalization.
- **Can Handle Nonlinear Relationships**: By splitting data into subsets, trees can model complex patterns.
- **Fast Training and Inference**: Efficient to train and make predictions compared to some more complex models.

---

## Limitations

- **Prone to Overfitting**: Trees can become too complex and fit noise in the data unless cut.
- **Unstable**: Small changes in data can lead to entirely different trees.
- **Algorithm Issues**: Makes locally optimal decisions that may not lead to the globally optimal tree.

---

## Real-World Applications

- **Customer Churn Prediction**: Deciding whether a customer is likely to leave a service.
- **Medical Diagnosis**: Predicting the presence or absence of disease based on symptoms.
- **Loan Approval**: Evaluating creditworthiness of loan applicants.
- **Sales Forecasting**: Estimating future revenue based on historical data.