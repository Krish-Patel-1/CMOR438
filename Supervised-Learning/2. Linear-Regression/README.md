# Linear Regression

**Linear Regression** is one of the simplest and most widely used supervised learning algorithms in machine learning. It is used to model the relationship between a **dependent variable (target)** and one or more **independent variables (features)** by fitting a linear equation to the observed data. The primary goal of linear regression is to find the **best-fit straight line**—also called a regression line—that minimizes the error between the predicted outputs and the actual data points.

In **simple linear regression**, the model assumes a straight-line relationship between a single input variable and the output, expressed as:

```
y = mx + b
```

Where:
- `y` is the predicted output (dependent variable),
- `x` is the input feature (independent variable),
- `m` is the slope of the line (coefficient),
- `b` is the y-intercept (bias term).

---

## Assumptions of Linear Regression

For linear regression to produce valid results, certain assumptions should be satisfied:

1. The relationship between input and output is linear.
2. Observations are independent of each other.
3. The variance of error terms is constant across all levels of the independent variables.
4. The residuals (errors) are normally distributed.

---

## Performance Evaluation

To assess the performance of a linear regression model, various metrics are used—most commonly the **Mean Squared Error (MSE)**:

### Mean Squared Error (MSE)

MSE measures the average of the squares of the errors—that is, the average squared difference between predicted and actual values.

```
MSE = (1/n) * Σ(yᵢ - ŷᵢ)²
```

Where:
- `yᵢ` is the actual value,
- `ŷᵢ` is the predicted value,
- `n` is the number of data points.

A lower MSE value indicates that the model predictions are closer to the actual values, meaning the regression line fits the data better. However, MSE **penalizes large errors more** severely due to squaring, which can exaggerate the impact of outliers or high-variance errors.

### Root Mean Squared Error (RMSE)

To mitigate the squared error effect, we often use **Root Mean Squared Error**, which is simply the square root of the MSE:

```
RMSE = √MSE
```

RMSE brings the error metric back to the same unit as the target variable, making it more interpretable. While it still emphasizes larger errors, it does so to a lesser extent than MSE.

---

## Advantages

- **Simple to implement and interpret**
- **Computationally efficient**
- **Works well for linearly related data**
- **Provides insights into feature influence via weights**

---

## Limitations

- Performs poorly with **non-linear relationships**
- Sensitive to **outliers** which can skew the regression line
- Assumes that all important features are **linearly related**
- Can be impacted by **multicollinearity** in multiple regression

---

## Applications

Linear regression is used in a wide range of domains, such as:

- **Predicting housing prices** based on features like size, location, and number of rooms
- **Forecasting sales** or financial performance over time
- **Medical research**, to predict disease progression based on patient metrics
- **Advertising analysis**, such as estimating the effect of spending on different platforms

---

## Linear vs Logistic Regression
Both are supervised learning models. However many differences are present including:
* Linear regression values are predicted by an integer while logistic is by 0 or 1
* Only logistic regression has a threshold value
* Linear regression is a linear line while logistic is an S-shaped curve
* Linear regression is used to estimate dependent variables if there is a change in the independent variables. Logistic regression is used for predicting the probability of something happening.