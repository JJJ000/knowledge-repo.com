---
title: What is the process of adding type hints to a generator in Python 3?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-17 00:00:00
updated_at: 2023-03-17 00:00:00
tldr: Use `-> Iterator` after the arguments in the function definition to type hint a generator in Python 3.
---

**Contents**

[TOC]

## Why use type hints?

Type hints are a way to give Python more information about the types of variables used in a program. They can help catch type-related errors before runtime and make code easier to read and maintain. Type hints can be added to variables, function parameters, and return values, and are especially useful in large and complex codebases.

## Generator basics

A generator in Python is a special type of iterator that generates values on-the-fly instead of storing them in memory like a list. Generators are implemented using the `yield` keyword, which allows a function to "pause" and remember its state so that it can resume execution from where it left off later.

For example, here is a simple generator that yields the first `n` even numbers:

```python
def even(n):
    for i in range(n):
        yield i*2
```

This generator can be used in a `for` loop like this:

```python
for num in even(5):
    print(num)
```

which will output:

```
0
2
4
6
8
```

## How to type hint a generator

To type hint a generator function or expression, we use the `Generator` type from the `typing` module. Here is an example:

```python
from typing import Generator

def even(n: int) -> Generator[int, None, None]:
    for i in range(n):
        yield i*2
```

In this example, we have added type hints for the `n` parameter as an `int`, and the generator type itself as a `Generator[int, None, None]`. The `Generator` type takes three arguments:

- The first argument is the type of value that the generator produces (`int` in this case).
- The second argument is the type of value that can be sent into the generator using the `send()` method (in this case, `None` because we are not using `send()`).
- The third argument is the type of value that the generator returns when it is closed (in this case, also `None`).

We can use this type hint to ensure that the generator produces integers and also to help IDEs and type-checkers provide better code suggestions and error messages.

## Type hints for generator expressions

Generator expressions are a shorthand syntax for creating generators. They are similar to list comprehensions, but use parentheses instead of square brackets, and evaluate lazily like generators instead of eagerly like lists. Here is an example:

```python
evens = (i*2 for i in range(5))
```

We can add type hints to this generator expression by wrapping it in a `Generator` type:

```python
evens: Generator[int, None, None] = (i*2 for i in range(5))
```

Again, we can see that the type hint specifies the type of value produced by the generator (`int`), the type of value that can be sent into the generator (not used here), and the type of value returned by the generator when it is closed (not used here).

Using type hints with generator expressions can help catch type errors and make code easier to read and maintain, especially when used in combination with other typing features like type aliases and union types.
