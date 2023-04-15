---
title: What is the advantage of using 2 * (i * i) instead of 2 * I * I in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The former is evaluated as a single operation, whereas the latter is evaluated as two separate operations.
---

**Contents**

[TOC]

### Compiler Optimization

When the Java compiler encounters an expression, it will try to optimize it before the code is executed. In this case, the compiler will recognize that the two expressions are equivalent and will optimize the first expression to the second one. This optimization can result in faster code execution.

### Arithmetic Operations

The first expression, 2 * (i * i), requires three arithmetic operations: multiplication, multiplication, and multiplication. The second expression, 2 * i * i, requires only two arithmetic operations: multiplication and multiplication. This means that the second expression will be faster since it requires fewer arithmetic operations.

### Memory Access

The first expression, 2 * (i * i), requires two memory accesses: one to retrieve the value of i and one to store the result of i * i. The second expression, 2 * i * i, requires only one memory access: to retrieve the value of i. This means that the second expression will be faster since it requires fewer memory accesses.

### Cache Memory

The second expression, 2 * i * i, is more likely to benefit from the processor's cache memory due to its simpler structure. Since the processor can access data from the cache memory faster than from RAM, this can result in faster code execution.
