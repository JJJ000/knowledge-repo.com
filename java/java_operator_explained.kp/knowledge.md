---
title: What is the function of the '->' arrow operator in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The arrow operator, `->`, is used in Java to access methods and fields of a class from a reference variable.
---

**Contents**

[TOC]

# Description
The arrow operator (->) is used in Java for lambda expressions. A lambda expression is a block of code that can be passed around to execute at a later time. The arrow operator is used to separate the parameters of a lambda expression from the body of the expression. 

# Syntax
The syntax of the arrow operator is as follows:

```
(parameters) -> {body}
```

The parameters are specified on the left side of the arrow operator, and the body of the lambda expression is specified on the right side. 

# Example
As an example, consider the following lambda expression:

```
(x, y) -> x + y
```

In this expression, the parameters are x and y, and the body is x + y. This lambda expression adds two numbers together. 

# Uses
Lambda expressions are commonly used to create anonymous functions, which can be passed as arguments to other functions. This allows for more concise code and makes it easier to pass functions around.
