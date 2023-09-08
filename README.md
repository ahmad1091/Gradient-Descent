# Gradient Descent for Binary Classification

## Introduction

This project implements the Gradient Descent algorithm for binary classification. The goal of this project is to find the decision boundary that separates two classes of data points. The two classes are represented by the colors red and blue, and the algorithm iteratively adjusts its parameters to minimize the classification error.

## Problem Statement

Imagine you have a dataset with two classes of data points, where each data point has two features (X1 and X2). You want to find a line (decision boundary) that separates these two classes effectively. This separation is crucial for various applications, such as spam email detection, medical diagnosis, and more.

## Implementation Details

### Sigmoid Activation Function

The `sigmoid` function calculates the sigmoid activation of a given input, which is a crucial part of logistic regression. It's defined as:

`𝜎(𝑥) = 1 / (1 + 𝑒^(-𝑥))`

### Output Formula
The `output_formula` function computes the prediction based on the input features, weights, and bias. It uses the sigmoid function as follows:

`𝑦̂ = 𝜎(𝑤1𝑥1 + 𝑤2𝑥2 + 𝑏)`

### Error Formula
The `error_formula` function calculates the error (log-loss) between the predicted value and the actual target value. It's defined as:

`𝐸𝑟𝑟𝑜𝑟(𝑦, 𝑦̂) = −𝑦 * log(𝑦̂) − (1 − 𝑦) * log(1 − 𝑦̂)`

### Update Weights
The `update_weights` function adjusts the model's weights and bias based on the error and learning rate. It's defined as:

`𝑤𝑖 ⟶ 𝑤𝑖 + 𝛼(𝑦 − 𝑦̂)𝑥𝑖`
`𝑏 ⟶ 𝑏 + 𝛼(𝑦 − 𝑦̂)`

### Training Function
The `train` function performs the training process using gradient descent. It iterates through the dataset for a specified number of epochs, updating the model's parameters to minimize the error. It also provides visualizations, including:

1. Updates on training loss and accuracy during each epoch.
2. A plot showing the data points and the evolving decision boundary during training.
3. A plot displaying the error (log-loss) over the training epochs.

## How to Use
To use this project, follow these steps:

1. Provide your dataset in a CSV file format similar to the provided 'data.csv'. Ensure that it contains two features (X1 and X2) and a binary target variable (0 or 1).

2. Set the desired number of `epochs` and the `learnrate` (learning rate) in the code.

3. Run the `train` function, passing your dataset, epochs, learning rate, and optional visualization settings.

4. Observe the training process and the final decision boundary.

## Conclusion
This Gradient Descent implementation for binary classification is a fundamental machine learning algorithm used for solving classification problems. By iteratively adjusting the model parameters, it successfully finds the decision boundary that separates two classes of data points. This project provides a practical and visual understanding of how the algorithm works and its convergence over training epochs.

