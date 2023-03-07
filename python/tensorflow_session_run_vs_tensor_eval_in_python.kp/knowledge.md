---
title: What distinguishes session.run() from tensor.eval() in tensorflow?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Session.run() is used to execute one or multiple operations or tensors in a TensorFlow graph, while Tensor.eval() is a shortcut to evaluate a single tensor in the current session.
---

**Contents**

[TOC]

Section 1: Introduction 
TensorFlow is a popular open-source library for machine learning, which enables you to create complex neural networks and models. The library works by creating a computational graph that defines the mathematical operations of the model. In this computational graph, you have tensors that represent the data and the operations that work on the data. There are several ways to execute the operations and obtain the data for the tensors, such as the Session.run() method and the Tensor.eval() method. In this article, we will look at the main differences between these two methods.

Section 2: Session.run()
The Session.run() method provides a way to execute the operations in the computational graph. It takes as input a list of operations or tensors that you want to evaluate, and it returns the result of these operations in the form of a list of output tensors. The Session.run() method requires you to first create a session object, which acts as an environment for running the operations. The session object is responsible for allocating the necessary resources, such as memory and CPU/GPU, for running the operations. Once you have defined the operations and created the session object, you can call the Session.run() method to execute the operations and obtain the output.

Section 3: Tensor.eval()
The Tensor.eval() method is a shortcut for evaluating a single tensor in the computational graph. It takes no arguments and returns the result of the tensor. Unlike the Session.run() method, it does not require you to create a session object explicitly. Instead, it uses the default session object that is created when you define the computational graph. This means that you can use Tensor.eval() without having to create a session object yourself.

Section 4: Main differences between Session.run() and Tensor.eval()
The main difference between Session.run() and Tensor.eval() is that the former is used to evaluate multiple tensors, while the latter is used to evaluate a single tensor. Another difference is that Session.run() requires you to create a session object explicitly and pass it as an argument to the method, while Tensor.eval() uses the default session object. Additionally, the Session.run() method allows you to evaluate operations as well as tensors, while Tensor.eval() can only be used to evaluate tensors. Therefore, if you need to evaluate multiple tensors or operations, you should use Session.run(). However, if you only need to evaluate a single tensor, Tensor.eval() is more convenient and requires less code.
