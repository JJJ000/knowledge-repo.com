---
title: Lambdas in Java 8, function.identity() or t->t
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Function.identity() is the preferred approach for mapping a value to itself in Java 8 lambdas.
---

**Contents**

[TOC]

### Function.identity()

Function.identity() is a static method in the java.util.function package that returns a function that always returns its input argument. This method can be used to avoid explicit lambda expressions when the identity function is to be used, such as in Stream operations.

### Java 8 Lambdas

Java 8 lambdas are anonymous functions that can be used as a more concise alternative to anonymous inner classes. Lambdas can be used to pass behavior as a parameter to a method, such as with the Stream API. They can also be used as a way to create a functional interface, which is an interface with a single abstract method.

### t->t

The expression t->t is an example of a lambda expression that can be used in Java 8. This expression is equivalent to the identity function, and can be used in place of the Function.identity() method. It is a concise way to define a function that returns its input argument.
