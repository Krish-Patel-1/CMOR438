# Linear Regression
Linear regression is an algorithm that learns from the dataset to map the most optimized linear function. This function is a best-fit straight line through the data points and assumes a linear relationship between the inputs and outputs.

To interpret the success of linear regression, Mean Squared Error (MSE) is used. It evaluates the performance of the algorithm by providing a quantifiable metric to represent the average squared difference between predicted and actual values. This metric determines how well the regression line fits the data points: lower MSE = better fit.

However, MSE gives more weight to large errors which can skew the metric to make it seem like it is worse. As a result, it may be useful to use Root Mean Squared Error (RMSE) which is the square root of MSE. This is also skewed by large errors, but not as much as MSE.

## Linear vs Logistic Regression
Both are supervised learning models. However many differences are present including:
* Linear regression values are predicted by an integer while logistic is by 0 or 1
* Only logistic regression has a threshold value
* Linear regression is a linear line while logistic is an S-shaped curve
* Linear regression is used to estimate dependent variables if there is a change in the independent variables. Logistic regression is used for predicting the probability of something happening.