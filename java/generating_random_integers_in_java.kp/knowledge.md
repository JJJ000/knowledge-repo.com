---
title: What is the syntax for producing random integers within a given range in Java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-23 00:00:00
updated_at: 2023-01-23 00:00:00
tldr: Use the `Math.random()` and `Math.floor()` methods to generate random integers within a specific range.
---

**Contents**

[TOC]

### Using Math.random()

1. Generate a random double between 0.0 and 1.0 using `Math.random()`.
2. Multiply the random double by the difference between the maximum and minimum range values.
3. Add the minimum range value to the result of step 2.
4. Convert the result of step 3 to an integer.

### Using Random

1. Create a `Random` object.
2. Use the `Random` object's `nextInt(int n)` method to generate a random number between 0 and the difference between the maximum and minimum range values.
3. Add the minimum range value to the result of step 2.
