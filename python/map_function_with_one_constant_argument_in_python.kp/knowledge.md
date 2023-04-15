---
title: How can the map function be used with multiple arguments when one of them needs to remain constant?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Use the lambda function to define the map function, and specify the argument that remains the same as a default argument in the lambda function.
---

**Contents**

[TOC]

## Introduction
Python's `map()` function is widely used to apply a certain function to all elements of an iterable, such as a list, and return a new list with the transformed values. It is commonly used for quick and efficient transformations. However, there may be situations where the function that you pass to `map()` requires additional arguments beyond the elements of the iterable. In this case, you can use the `functools.partial()` function to bind specific arguments to the function, thus creating a new function that takes only the remaining arguments.

## Using `functools.partial()`
The `functools.partial()` function provides a way to create a new function with pre-filled arguments. This can be useful when you want to pass a function to `map()` that requires one or more additional arguments. Here's an example:

```python
import functools

def multiply(x, y):
    return x * y

x_values = [1, 2, 3, 4, 5]
y_value = 2

mul_by_two = functools.partial(multiply, y=y_value)
result = list(map(mul_by_two, x_values))

print(result)
```

This code creates a new function `mul_by_two`, which has the `y` argument pre-filled with the value `2`. Then, the `map()` function is called with `mul_by_two` and a list of `x` values. This produces a new list with the results of multiplying each `x` value by `2` (corresponding to `y_value`).

## Using `lambda` functions
Another way to use multiple arguments with the `map()` function is to provide a `lambda` function that can take multiple arguments. Here's an example:

```python
x_values = [1, 2, 3, 4, 5]
y_value = 2

result = list(map(lambda x: multiply(x, y_value), x_values))

print(result)
```

This code uses a `lambda` function to create a temporary function that takes an `x` value and multiplies it by `y_value`. The `map()` function then applies the `lambda` function to each `x` value in the list and returns a new list with the transformed values.

## Using `zip()` function
Finally, you can also use the `zip()` function to combine the `x` and `y` values into tuples, and then use a `lambda` function to transform each tuple. Here's an example:

```python
x_values = [1, 2, 3, 4, 5]
y_value = 2

result = list(map(lambda xy: multiply(xy[0], xy[1]), zip(x_values, [y_value]*len(x_values))))

print(result)
```

This code first creates a list of `y` values that is the same length as the list of `x` values. Then, the `zip()` function combines the two lists into tuples, where each tuple contains an `x` value and a corresponding `y` value. The `map()` function then applies a `lambda` function to each tuple, multiplying the `x` and `y` values together, and returns a new list with the transformed values.

## Conclusion
In conclusion, there are different ways to use multiple arguments with the `map()` function in Python, such as `functools.partial()`, `lambda` functions, and the `zip()` function. The choice depends on the specific use case and personal preference.
