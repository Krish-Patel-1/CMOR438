# The Perceptron
The perceptron is a type of neural network that performs binary classification that maps input features to an output decision.
---
## Parts of the Perceptron
The following data is courtesy of the website from this: [link](geeksforgeeks.org/machine-learning/what-is-perceptron-the-simplest-artificial-neural-network/)
The perceptron is composed of:
* Input Features: The perceptron takes multiple input features, each representing a characteristic of the input data.
* Weights: Each input feature is assigned a weight that determines its influence on the output. These weights are adjusted during training to find the optimal values.
* Summation Function: The perceptron calculates the weighted sum of its inputs, combining them with their respective weights.
* Activation Function: The weighted sum is passed through the Heaviside step function, comparing it to a threshold to produce a binary output (0 or 1).
* Output: The final output is determined by the activation function, often used for binary classification tasks.
* Bias: The bias term helps the perceptron make adjustments independent of the input, improving its flexibility in learning.
* Learning Algorithm: The perceptron adjusts its weights and bias using a learning algorithm, such as the Perceptron Learning Rule, to minimize prediction errors. 
---
## How the Perceptron works
A weight is assigned to each input node of a perceptron, indicating the importance of that input in determining the output. The Perceptron’s output is calculated as a weighted sum of the inputs, which is then passed through an activation function to decide whether the Perceptron will fire.

During training, the Perceptron's weights are adjusted to minimize the difference between the predicted output and the actual output. This is achieved using supervised learning algorithms like the delta rule or the Perceptron learning rule.

This process enables the perceptron to learn from data and improve its prediction accuracy over time.

