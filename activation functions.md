# Activation Functions in Neural Networks

## Table of Contents
1. [Introduction](#introduction)
2. [Common Activation Functions](#common-activation-functions)
    - [Sigmoid](#sigmoid)
    - [Tanh](#tanh)
    - [ReLU (Rectified Linear Unit)](#relu-rectified-linear-unit)
    - [Leaky ReLU](#leaky-relu)
    - [PReLU (Parametric ReLU)](#prelu-parametric-relu)
    - [ELU (Exponential Linear Unit)](#elu-exponential-linear-unit)
    - [Swish](#swish)
3. [Choosing an Activation Function](#choosing-an-activation-function)
4. [Conclusion](#conclusion)

## Introduction

Activation functions play a crucial role in neural networks by introducing non-linearity into the model, allowing it to learn complex patterns. This document provides an overview of common activation functions used in neural networks, their mathematical formulations, and their respective advantages and disadvantages.

## Common Activation Functions

### Sigmoid

- **Formula**: 
  \[
  \sigma(x) = \frac{1}{1 + e^{-x}}
  \]
- **Range**: (0, 1)
- **Advantages**:
  - Smooth gradient.
  - Output values bound between 0 and 1, useful for probabilistic interpretation.
- **Disadvantages**:
  - Vanishing gradient problem.
  - Outputs not zero-centered.

### Tanh

- **Formula**: 
  \[
  \tanh(x) = \frac{e^x - e^{-x}}{e^x + e^{-x}}
  \]
- **Range**: (-1, 1)
- **Advantages**:
  - Zero-centered outputs.
  - Stronger gradients than sigmoid.
- **Disadvantages**:
  - Vanishing gradient problem.

### ReLU (Rectified Linear Unit)

- **Formula**: 
  \[
  \text{ReLU}(x) = \max(0, x)
  \]
- **Range**: [0, ∞)
- **Advantages**:
  - Computationally efficient.
  - Reduces likelihood of vanishing gradients.
- **Disadvantages**:
  - Dying ReLU problem (neurons can become inactive).

### Leaky ReLU

- **Formula**: 
  \[
  \text{Leaky ReLU}(x) = \begin{cases} 
  x & \text{if } x > 0 \\
  \alpha x & \text{if } x \le 0 
  \end{cases}
  \]
  where \(\alpha\) is a small constant (e.g., 0.01).
- **Range**: (-∞, ∞)
- **Advantages**:
  - Fixes dying ReLU problem.
- **Disadvantages**:
  - Results are not consistent with all types of data.

### PReLU (Parametric ReLU)

- **Formula**: 
  \[
  \text{PReLU}(x) = \begin{cases} 
  x & \text{if } x > 0 \\
  \alpha x & \text{if } x \le 0 
  \end{cases}
  \]
  where \(\alpha\) is a learnable parameter.
- **Range**: (-∞, ∞)
- **Advantages**:
  - Learnable parameter allows for better fitting.
- **Disadvantages**:
  - Can lead to overfitting.

### ELU (Exponential Linear Unit)

- **Formula**: 
  \[
  \text{ELU}(x) = \begin{cases} 
  x & \text{if } x > 0 \\
  \alpha (e^x - 1) & \text{if } x \le 0 
  \end{cases}
  \]
  where \(\alpha\) is a hyperparameter.
- **Range**: (-α, ∞)
- **Advantages**:
  - Helps mitigate the vanishing gradient problem.
  - Negative saturation for negative inputs.
- **Disadvantages**:
  - Computationally more expensive than ReLU.

### Swish

- **Formula**: 
  \[
  \text{Swish}(x) = x \cdot \sigma(x)
  \]
- **Range**: (-∞, ∞)
- **Advantages**:
  - Smooth, non-monotonic function.
  - Shows better performance in deep networks.
- **Disadvantages**:
  - Computationally more complex.

## Choosing an Activation Function

The choice of activation function depends on the specific problem and the architecture of the neural network. Here are some guidelines:
- **Sigmoid/Tanh**: Generally used in the output layer for binary classification.
- **ReLU**: Widely used in hidden layers of deep neural networks.
- **Leaky ReLU/PReLU**: Useful when ReLU fails due to the dying ReLU problem.
- **ELU/Swish**: Can be beneficial in deeper networks to avoid vanishing gradients and improve training dynamics.

## Conclusion

Activation functions are key to the performance of neural networks. Understanding their properties and selecting the appropriate one for your model can significantly impact the effectiveness of the learning process. Experimentation and empirical results often guide the final choice.

---

Feel free to contribute to this document by adding more activation functions or suggesting improvements. 