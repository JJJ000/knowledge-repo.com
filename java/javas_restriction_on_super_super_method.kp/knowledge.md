---
title: Why is it not possible to use multiple levels of inheritance in a single method call in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Super.super.method(); is not allowed in Java because it is not possible to access a parent class` parent class` methods directly.
---

**Contents**

[TOC]

### Reasons

1. Java does not support multiple inheritance, which is required to use `super.super.method()`.
2. Java does not allow access to the parent class of a parent class. 

### Explanation

In Java, the `super` keyword is used to access members of the parent class. The `super` keyword can only be used to access the immediate parent class. This means that `super.super.method()` is not allowed because it would require accessing the parent class of the parent class, which is not supported by Java. 

### Alternatives

If the desired functionality requires accessing a parent class of a parent class, one alternative is to use composition instead of inheritance. This involves creating a class that contains an instance of the parent class, and then accessing the parent class methods through that instance. Another alternative is to use interfaces, which allow multiple inheritance in Java.
