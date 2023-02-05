---
title: Round to the nearest whole number
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The round() function can be used to round a number to its nearest integer in Python.
---

**Contents**

[TOC]

## Using the `round()` Function

The `round()` function in Python is used to round a number to the nearest integer. To use this function, you pass in the number you want to round and the number of decimal places you want the result to have.

For example,

```python
x = 3.6

rounded_x = round(x)
```

The value of `rounded_x` would be `4`.

## Using the `math.ceil()` Function

Another way to round a number to the nearest integer is to use the `math.ceil()` function. This function takes a single argument, the number you want to round, and returns the smallest integer greater than or equal to the argument.

For example,

```python
x = 3.6

rounded_x = math.ceil(x)
```

The value of `rounded_x` would be `4`.

## Using the `math.floor()` Function

The `math.floor()` function is similar to the `math.ceil()` function, but instead of returning the smallest integer greater than or equal to the argument, it returns the largest integer less than or equal to the argument.

For example,

```python
x = 3.6

rounded_x = math.floor(x)
```

The value of `rounded_x` would be `3`.

## Using the `int()` Function

The `int()` function can also be used to round a number to the nearest integer. This function takes a single argument, the number you want to round, and returns the integer that is closest to the argument.

For example,

```python
x = 3.6

rounded_x = int(x)
```

The value of `rounded_x` would be `3`.
