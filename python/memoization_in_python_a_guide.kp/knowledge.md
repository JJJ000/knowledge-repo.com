---
title: Could you explain what memoization is and provide an example of how to implement it in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Memoization is a technique used to store the results of expensive function calls, allowing for faster subsequent calls by reusing the cached results, and it can be implemented in Python using a decorator.
---

**Contents**

[TOC]

### What is Memoization?
Memoization is a programming technique which attempts to increase a function’s performance by caching its previously computed results. This technique is most commonly used when a function is called multiple times with the same input parameters. By storing the results of these calls, the function can avoid doing the same work over again and instead quickly return the cached result.

### Benefits of Memoization
The primary benefit of memoization is improved performance. By caching the results of expensive function calls, memoization can drastically reduce the amount of time needed to compute the same result multiple times. This can be especially beneficial when dealing with large datasets or recursive functions.

### How to Use Memoization in Python
Memoization can be implemented in Python using a simple dictionary. The dictionary is used to store the results of each function call, with the input parameters as the key. Every time the function is called, the dictionary is checked to see if the result for the given input parameters is already stored. If so, the stored result is returned, otherwise the function is executed and the result is stored in the dictionary.

### Example
The following example uses memoization to calculate the nth Fibonacci number.

```
# Fibonacci sequence using memoization
def fib(n, memo={}):
    if n in memo:
        return memo[n]
    if n <= 2:
        f = 1
    else:
        f = fib(n-1, memo) + fib(n-2, memo)
    memo[n] = f
    return f

print(fib(10))
```

In this example, the dictionary `memo` is used to store the results of each function call. Each time the function is called, the dictionary is checked to see if the result for the given input parameter (`n`) is already stored. If so, the stored result is returned, otherwise the function is executed and the result is stored in the dictionary.
