# Decision and Regression Trees

---

A decision tree follows a hierarchical, tree-like structure composed of a root node, branches, internal nodes, and leaf nodes.

The tree begins with a root node that has no incoming branches. From the root, branches lead to internal nodes, also called decision nodes. At these nodes, decisions are made based on the available features, and the data is split into subsets. These internal nodes continue this process until they reach the leaf nodes, also known as terminal nodes, which represent the final outcomes of the data. Each leaf node corresponds to a possible outcome within the dataset.

Decision tree learning applies a divide-and-conquer approach, using a greedy algorithm to search for the best split points within the tree. This process is recursively carried out in a top-down fashion until most, or all, of the records are assigned to specific class labels.

In the case of regression trees, the target variables are continuous rather than categorical. As a result, regression trees use modified criteria for selecting splits and determining when to stop growing the tree.