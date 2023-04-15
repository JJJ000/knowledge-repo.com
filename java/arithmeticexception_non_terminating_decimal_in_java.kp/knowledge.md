---
title: Arithmeticexception decimal expansion is infinite and there is no exact decimal representation of the result
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: An ArithmeticException is thrown when a decimal expansion cannot be represented exactly in Java.
---

**Contents**

[TOC]

### What is an ArithmeticException?
An ArithmeticException is an exception type in Java that is thrown when an exceptional arithmetic condition has occurred. It is a subclass of RuntimeException and is thrown when an exceptional arithmetic condition has occurred.

### What is a Non-Terminating Decimal Expansion?
A non-terminating decimal expansion is a decimal representation of a number that does not terminate, meaning that it does not end after a certain number of digits. This can happen when the number is irrational, such as pi or the square root of two.

### What Does "No Exact Representable Decimal Result" Mean?
When a non-terminating decimal expansion is encountered, it is impossible to represent it exactly in decimal form. This means that the number cannot be represented accurately with a finite number of digits.

### Why Does this Cause an ArithmeticException?
The ArithmeticException is thrown when a non-terminating decimal expansion is encountered and there is no exact representable decimal result. This is because the decimal representation of the number cannot be accurately represented in decimal form, and so the exception is thrown.
