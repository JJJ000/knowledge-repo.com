---
title: Lambda expression with no arguments in Java 8
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: A lambda expression with a void argument must accept no argument and return no value.
---

**Contents**

[TOC]

1. Overview
----------------
Java 8 Lambda expressions are used to represent an anonymous function with a single argument. In some cases, the argument may be of type void, meaning that the function does not take any arguments. This article will discuss the use of Java 8 Lambda expressions with a void argument.

2. Syntax
----------------
The syntax of a Java 8 Lambda expression with a void argument is as follows: 

`( ) -> { // Code block }`

The parentheses indicate that the function does not take any arguments. The code block is the body of the function, which will be executed when the function is called.

3. Example
----------------
An example of a Java 8 Lambda expression with a void argument is as follows: 

`() -> { System.out.println("Hello World!"); }`

This Lambda expression prints the string "Hello World!" when it is called.

4. Conclusion
----------------
Java 8 Lambda expressions can be used with a void argument to represent an anonymous function that does not take any arguments. The syntax of a Lambda expression with a void argument is simple and straightforward, and an example of such an expression has been provided.
