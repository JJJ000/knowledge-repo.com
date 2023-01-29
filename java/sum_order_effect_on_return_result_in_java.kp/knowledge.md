---
title: What is the effect of changing the order of the numbers in an equation on the outcome?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The order of operations matters in Java, so changing the order of the summands can cause a different result.
---

**Contents**

[TOC]

### Floating Point Error

When adding two numbers together in Java, the result may not be the same if the order of the numbers is changed. This is due to the fact that Java stores numbers as floating point values, which can cause small errors in the result.

### Rounding Error

When two numbers are added together, the result may be rounded to the nearest whole number. This can cause a difference in the result if the order of the numbers is changed, as the rounding may be done differently depending on the order.

### Floating Point Representation

The way that Java stores numbers as floating point values can also cause a difference in the result if the order of the numbers is changed. This is because the way that the numbers are represented in memory can affect the result of the calculation.

### Compiler Optimization

The compiler may also optimize the code differently depending on the order of the numbers. This can cause a difference in the result if the order of the numbers is changed, as the compiler may optimize the code in a way that produces a different result.
