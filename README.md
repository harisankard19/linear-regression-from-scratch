# linear-regression-from-scratch

Implementing a linear regression model from scratch is a strong foundational exercise. It helps you understand how optimization works, especially gradient descent and loss minimization. By manually computing weights, bias, and errors, you internalize the math behind model fitting. This builds intuition for more complex models and gives you full control over every step, which high-level libraries abstract away. It's not for production use but critical for learning.

Usage:

load the Linear_Regression class to colab, then execute:      from Linear_Regression import Linear_Regression 



1. What is Linear Regression?
Linear regression tries to model the relationship between input features (X) and a continuous target (y) using a straight line. It finds the best-fit line that minimizes the difference between predicted and actual values.

2. Parameters:
These are the values the model learns from data. In linear regression, parameters include:

Weights (w) – also called coefficients; they scale each input feature.

Bias (b) – a constant added to the output, allowing the model to fit data not passing through the origin.

For one input:


y_pred = w * x + b

For multiple inputs:


y_pred = w1*x1 + w2*x2 + ... + wn*xn + b

3. Weights:
These determine how much influence each input feature has on the output.

Initialized randomly or with zeros.

Learned by minimizing the loss during training.

4. Bias:
A scalar added to the weighted sum.

Allows the model to adjust the output up/down regardless of input values.

5. Learning Rate (LR):
A small positive value controlling how big each update step is during training.

Too high → model diverges.

Too low → training becomes very slow.

6. Training Process:
Compute predictions using current weights and bias.

Measure error using a loss function (usually Mean Squared Error).

Use gradient descent to adjust weights and bias to reduce the loss.

7. Loss Function:
For MSE:

Loss = (1/n) * Σ(y_pred - y_actual)^2
Gradient descent calculates how much to change each parameter to reduce this loss, and updates them:

w = w - lr * dL/dw
b = b - lr * dL/db
