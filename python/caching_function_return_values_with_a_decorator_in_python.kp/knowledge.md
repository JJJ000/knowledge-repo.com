---
title: Is it possible to find a decorator that could easily cache the return values of a function?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Yes, Python provides the `functools.lru\_cache` decorator for caching function return values.
---

**Contents**

[TOC]

Yes, there is a decorator to cache function return values in Python.

## Memoization

The decorator is called memoization. Memoization is a technique that stores the results of expensive function calls and returns the cached result when the same inputs occur again.

Here is an example of how to use memoization in Python:

```python
import functools

@functools.lru_cache(maxsize=None)
def expensive_function(*args, **kwargs):
    ...
```

The `lru_cache` decorator is part of the `functools` module in Python. It takes an optional argument `maxsize` to limit the size of the cache. If `maxsize` is set to `None` (the default), the cache can grow without limit.

The decorator can be applied to any function. When the function is called with the same arguments as before, the cached result is returned instead of executing the function again.

Memoization is a simple and effective way to speed up Python programs that make expensive function calls.

## Example

Here is an example of how to use memoization to cache the result of a Fibonacci sequence function:

```python
import functools

@functools.lru_cache(maxsize=None)
def fib(n):
    if n < 2:
        return n
    return fib(n-1) + fib(n-2)

print(fib(50))  # prints 12586269025
```

The `fib` function is defined recursively, which is an expensive operation for large values of `n`. By applying the `lru_cache` decorator, we can cache the results of previous calls and avoid unnecessary calculations.

## Limitations

Memoization is a powerful tool, but it has some limitations:

* The cache can consume a lot of memory if the function is called with many different arguments.
* The function must be pure, which means it always returns the same output given the same input. If the function has side effects or relies on external state, memoization may produce unexpected results.
* The cache can be invalidated if the function's arguments are mutable (e.g. a list or dictionary) and the values change between calls.

Despite these limitations, memoization is a useful technique for optimizing Python programs that perform expensive computations.
