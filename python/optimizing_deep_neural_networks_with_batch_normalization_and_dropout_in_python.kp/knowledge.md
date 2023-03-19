---
title: What is the sequence for applying batch normalization and dropout techniques?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Batch normalization should be applied before dropout during training while during inference, the order isn`t important.
---

**Contents**

[TOC]

## Introduction

Batch normalization and dropout are two techniques commonly used in neural networks to improve their performance. In this article, we will discuss the ordering of batch normalization and dropout and the reasons behind it. 

## Batch Normalization 

Batch normalization is a technique used to improve the training of artificial neural networks. It normalizes the input layer by subtracting the mean and dividing by the standard deviation, thus making the inputs zero-mean and with unit variance. Batch normalization has been found to improve training speed, stability, and accuracy. 

## Dropout 

Dropout is a regularization technique that helps prevent overfitting in neural networks. It works by randomly ignoring or "dropping out" some neurons during training, thereby reducing their contribution to the output. Dropout has been found to improve generalization and reduce overfitting. 

## Ordering of Batch Normalization and Dropout 

The order in which batch normalization and dropout are applied can affect the performance of the neural network. The order can be summarized as follows:

1. Batch normalization before dropout: Applying batch normalization before dropout has been found to be the most effective way of using the two techniques together. This is because batch normalization normalizes the inputs, which helps to reduce the impact of dropout. 

2. Dropout before batch normalization: Applying dropout before batch normalization can cause the network to learn incorrect statistics, which can reduce the effectiveness of batch normalization. 

3. Batch normalization and dropout between layers: It is generally recommended to apply batch normalization and dropout between layers rather than within layers. This is because applying batch normalization and dropout within layers can produce inconsistent results due to the alteration of individual neurons' values. 

4. Batch normalization and dropout after activation functions: It is generally recommended to apply batch normalization and dropout after the activation functions. This is because applying them before activation can alter the input distribution, leading to reduced performance. 

## Conclusion 

In this article, we have discussed the ordering of batch normalization and dropout in neural networks. Applying batch normalization before dropout is generally considered the best practice. Additionally, it is recommended to apply them between layers and after the activation functions, while applying them before activation may lead to reduced performance.
