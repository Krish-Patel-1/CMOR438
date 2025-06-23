# Boosting
Boosting is an ensemble learning method that sequentially trains predictors by making weak learners into strong learners to minimize training errors. I will be focusing on the AdaBoost method.

The AdaBoost algorithm trains a base classifier and then uses it to make predictions on the training set. Relative weights are given to each misclassified training instance. This is repeated so that if a classifier misclassifies a data point, the data point is boosted to signal difficulty in the classification process.