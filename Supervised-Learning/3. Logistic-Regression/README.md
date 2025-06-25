# Logistic Regression

**Logistic Regression** is a supervised machine learning algorithm used primarily for **binary classification** tasks. Unlike linear regression, which predicts a continuous value, logistic regression predicts the **probability** that a given input belongs to a specific category, such as "yes" or "no", "spam" or "not spam", or "disease" vs. "no disease". 

It is particularly useful when the dependent variable is **categorical** in nature (commonly binary: 0 or 1). Instead of fitting a straight line, logistic regression fits an **S-shaped curve** (sigmoid function) to the data.

---

## The Logistic Function (Sigmoid Function)

At the core of logistic regression lies the **logistic function**, also known as the **sigmoid function**, which transforms any real-valued number into a value between 0 and 1:

```
σ(z) = 1 / (1 + e^(-z))
```

Where:
- `z = w₁x₁ + w₂x₂ + ... + wₙxₙ + b` is the linear combination of input features and weights,
- `e` is the base of the natural logarithm,
- `σ(z)` represents the predicted **probability** of the positive class.

This output is interpreted as the **probability** that the input belongs to the positive class (e.g., class = 1).

---

## Classification Threshold

The sigmoid function outputs a probability between 0 and 1. To make a final classification decision, a **threshold** is applied—commonly 0.5:

- If `σ(z) ≥ 0.5` → classify as **positive** (1)
- If `σ(z) < 0.5` → classify as **negative** (0)

The threshold can be adjusted depending on the problem. 

---

## Advantages

- Provides probability scores, not just class labels.
- Easy to implement and computationally fast.
- Based on solid statistical foundations.
- Coefficients can be interpreted to understand feature impact.

---

## Limitations

- Assumes a **linear decision boundary** between classes.
- Can underperform on **complex or non-linear datasets**.
- Sensitive to **outliers** and **multicollinearity**.
- Not ideal for **multi-class problems** without extension (e.g., softmax regression).

---

## Applications

Logistic regression is widely used in:

- **Medical diagnosis**: Predicting presence/absence of a disease
- **Email filtering**: Spam detection
- **Credit scoring**: Classifying loan applications as default or safe
- **Marketing**: Predicting whether a customer will respond to a campaign
- **Fraud detection**: Flagging potentially fraudulent transactions

---

## Linear vs Logistic Regression
Both are supervised learning models. However many differences are present including:
* Linear regression values are predicted by an integer while logistic is by 0 or 1
* Only logistic regression has a threshold value
* Linear regression is a linear line while logistic is an S-shaped curve
* Linear regression is used to estimate dependent variables if there is a change in the independent variables. Logistic regression is used for predicting the probability of something happening.