---
title: Is it true that using for-loops in pandas is not recommended? when should it be taken into consideration?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: For-loops in pandas can be slow when working with large datasets, and you should care about it when dealing with performance-critical tasks.
---

**Contents**

[TOC]

Why for-loops in Pandas can be slow

When using Pandas, it is generally preferable to avoid using for-loops wherever possible, as they can be slow when working with larger datasets. This is because each iteration of the loop results in a new Pandas DataFrame or Series being created, which can lead to expensive memory allocation and deallocation operations. Additionally, Python's global interpreter lock (GIL) can make parallel execution with for-loops slower.

Alternatives to for-loops in Pandas

In order to avoid using for-loops in Pandas, you can use many built-in functions to optimize code execution. For example, vectorized functions like apply() and applymap() can be used in many instances rather then using a for loop. While iterrows() and itertuples() is another alternative to for loops in case one need to perform a row wise operation.

When to use for-loops in Pandas

Despite being slower than some alternatives, there are still some scenarios in which using for-loops in Pandas is necessary or justified. For example, if you need to manipulate individual rows based on certain conditions and the amount of data being processed is small enough, then using for loop can be a reasonable choice. 

When to use Numba

Numba allows accelerated computations with Python for-loops, but works only with vectorization of the code. It achieves this by producing optimized machine code, which eliminates interpreter overhead. It is worth a try when one need to run n unmber of iterations on an array of low dimension.
