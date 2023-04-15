---
title: Is there a counterpart of sum() that can be used for multiplication? is it product()?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Yes, the function in Python that is similar to sum() but for multiplication is called product().
---

**Contents**

[TOC]

Introduction
------------
Python has built-in functions to perform mathematical operations like addition, subtraction, multiplication, and division. Among these functions, `sum()` is a built-in Python function that returns the sum of elements in a list or tuple. Is there any similar function for multiplication? The answer is yes. In Python, we can use the built-in function `product()` to perform multiplication of elements in a list or tuple.

Product()
----------
The `product()` function is used to calculate the product of all the elements in a list or tuple. It takes an iterable as an argument and returns the product of all elements in the iterable.

Syntax: `product(iterable, start=1)`

- `iterable`: An iterable (list, tuple, set, etc.) containing numbers to calculate the product.
- `start`: An optional argument to set the starting value of the product. Its default value is 1.

Example:

```python
from functools import product

result = product([2, 3, 4])
print(result)  # Output: 24
```

Here, the `product()` function takes a list `[2, 3, 4]` as input and returns the product of all elements, i.e., `2 * 3 * 4` = 24.

Using a Starting Value
----------------------
We can also provide a starting value to the `product()` function using the `start` parameter.

Example:

```python
from functools import product

result = product([2, 3, 4], 5)
print(result)  # Output: 120
```

Here, the `product()` function takes a list `[2, 3, 4]` and a starting value `5` as input and returns the product of all elements after multiplying it with the starting value, i.e., `5 * 2 * 3 * 4` = 120.

Handling Empty iterables
------------------------
If the iterable passed to `product()` is empty, it returns the starting value (1 by default).

Example:

```python
from functools import product

result = product([])
print(result)  # Output: 1
```

Here, an empty list is passed to the `product()` function, and it returns the starting value, which is 1 by default.
