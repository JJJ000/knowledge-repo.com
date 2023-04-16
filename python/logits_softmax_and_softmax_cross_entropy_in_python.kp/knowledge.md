---
title: What are logits? logits are a vector of raw (non-normalized) predictions that a classification model generates, which is ordinarily then passed to a normalization function. 

what is the difference between softmax and softmax_cross_entropy_with_logits? softmax is a normalization function that takes the logits vector and transforms it into a probability distribution, where each element represents the probability of the input belonging to a certain class. softmax_cross_entropy_with_logits is a loss function that combines the softmax function with cross entropy loss. it takes the logits vector and the desired output class as inputs and produces a single scalar value that represents the loss
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Logits are raw, unnormalized values that represent the output of a neural network before being passed through the softmax activation function. Softmax is an activation function which outputs the probability of each class, while softmax\_cross\_entropy\_with\_logits is a loss function which combines the softmax activation function with the cross-entropy loss for multi-class classification.
---

**Contents**

[TOC]

## What are Logits?
Logits are the unnormalized output of a neuron in a neural network. They are used to measure the probability of an event occurring and are calculated by applying a linear transformation (usually a matrix multiplication) to the input of the neuron. Logits are typically used in classification tasks, where they are used to measure the probability of a given input belonging to a certain class.

## Softmax
Softmax is an activation function used in neural networks to normalize the outputs of a neuron, so that they sum up to one. This allows the output of a neuron to be interpreted as a probability distribution, where the output of the softmax function is a vector of probabilities, with each element representing the probability of the corresponding class.

## Softmax Cross Entropy with Logits
Softmax cross entropy with logits is a loss function used for training neural networks. It is a combination of the softmax activation function and the cross-entropy loss function. The softmax function is used to normalize the output of the neuron, and the cross-entropy loss is used to measure the difference between the predicted output and the true output. The logits are used as the input to the softmax activation function, and the output of the softmax function is then used as the input to the cross-entropy loss function.
