# The Perceptron

The **Perceptron** is one of the earliest and most fundamental types of artificial neural networks, designed for **binary classification tasks**. It maps a set of input features to a single binary output by learning appropriate weights during training. 

---

## Parts of the Perceptron

(Information partially referenced from [GeeksforGeeks](https://www.geeksforgeeks.org/machine-learning/what-is-perceptron-the-simplest-artificial-neural-network/))

A Perceptron consists of several key components that work together to produce a binary classification output:

### 1. Input Features
These are the raw data points fed into the model. Each feature represents a measurable property or characteristic of the input data. The Perceptron can accept multiple features, such as pixel intensities in an image or measurements in a dataset.

### 2. Weights
Each input feature is associated with a numerical weight. These weights signify the **importance** or **influence** of each feature on the final decision. Initially, weights are assigned randomly and updated through training.

### 3. Bias
The bias is an additional parameter that allows the activation function to shift left or right. This improves the model’s ability to generalize and helps it learn patterns that do not necessarily pass through the origin.

### 4. Summation Function
The summation function computes the **weighted sum** of all input features. Mathematically, this is represented as:

```
z = ∑ (wᵢ * xᵢ) + b
```

where `wᵢ` are the weights, `xᵢ` are the input features, and `b` is the bias.

### 5. Activation Function
After summation, the result `z` is passed through an **activation function**, which determines the output of the Perceptron. Traditionally, the **Heaviside step function** is used:

```
f(z) = 1 if z ≥ Threshold  
       0 if z < Threshold
```

This function outputs either a 0 or 1, making it suitable for binary classification.

### 6. Output
The final binary output of the perceptron is the result of the activation function. It can represent two different classes such as *spam vs. not spam*, *positive vs. negative sentiment*, or *cat vs. dog*.

### 7. Learning Algorithm
The learning algorithm updates the weights and bias based on the error in the prediction. The **Perceptron Learning Rule** is used to reduce the prediction error by adjusting the weights according to the difference between the actual and predicted outputs. This process is iterated over multiple training examples.

---

## How the Perceptron Works

The working mechanism of the Perceptron follows a clear and structured pattern:

1. **Initialization**  
   Weights and bias are initialized to small random values or zeros.

2. **Forward Pass**  
   For each training example, the weighted sum of inputs is calculated and passed through the activation function to generate a prediction.

3. **Error Calculation**  
   The difference between the predicted output and the actual target value (label) is computed.

4. **Weight Update**  
   If the prediction is incorrect, the weights and bias are updated using the **Perceptron Learning Rule**:

```
wᵢ ← wᵢ + η * (y - ŷ) * xᵢ
```

- `η`: learning rate  
- `y`: actual output  
- `ŷ`: predicted output  
- `xᵢ`: input feature

5. **Iteration**  
   This process continues over multiple epochs (passes through the training data) until the model converges or achieves an acceptable accuracy.

---

## Limitations of the Perceptron

While foundational, the Perceptron has its limitations:

- It can only solve **linearly separable** problems.
- The use of a step function limits the Perceptron from learning complex decision boundaries due to its non-differentiability.

---

## Applications

Despite its simplicity, the Perceptron has practical value in:

- **Email spam detection**
- **Image recognition for simple tasks**
- **Sentiment classification (positive/negative)**
- **Pattern recognition in sensor or biometric data**
- **Educational purposes** to introduce the fundamentals of machine learning