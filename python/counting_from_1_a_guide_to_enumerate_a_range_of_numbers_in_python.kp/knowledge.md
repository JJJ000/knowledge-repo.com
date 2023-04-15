---
title: What is the procedure for listing a set of numbers beginning with 1?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Use the function `range()` with a starting value of 1 and an upper limit, such as `range(1, 10)`, to enumerate a range of numbers starting at 1 in Python.
---

**Contents**

[TOC]

## Using the range() function

The most commonly used method to enumerate a range of numbers starting at 1 in Python is by using the `range()` function. The built-in `range()` function in Python generates a sequence of numbers starting from 0 by default, but can be used to generate a range of numbers starting from a different value by adding an argument for the starting value. 

Here is an example of how to use the `range()` function to enumerate a range of numbers starting at 1:

```python
for i in range(1, 10):
    print(i)
```

In this example, `range(1, 10)` generates a sequence of numbers starting at 1 and ending at 9 (because the second argument in `range()` is exclusive), and the `for` loop iterates over each number in the sequence and prints it to the console.

## Using a while loop

Another way to enumerate a range of numbers starting at 1 in Python is by using a `while` loop. 

Here is an example of how to use a `while` loop to enumerate a range of numbers starting at 1:

```python
i = 1
while i < 10:
    print(i)
    i += 1
```

In this example, the `while` loop will continue to iterate as long as `i` is less than 10. 

## Using a list comprehension

A list comprehension is a concise way to generate a list in Python. It can also be used to enumerate a range of numbers starting at 1.

Here is an example of how to use a list comprehension to enumerate a range of numbers starting at 1:

```python
numbers = [i for i in range(1, 10)]
print(numbers)
```

In this example, the list comprehension `[i for i in range(1, 10)]` generates a list of numbers starting at 1 and ending at 9, and the `print()` function prints the list to the console.

## Using numpy.arange()

Lastly, we can use numpy's `arange()` function to enumerate a range of numbers starting at 1 in Python.

Here is an example of how to use `arange()` to enumerate a range of numbers starting at 1:

```python
import numpy as np

numbers = np.arange(1, 10)
print(numbers)
```

In this example, `np.arange(1, 10)` generates a numpy array of numbers starting at 1 and ending at 9, and the `print()` function prints the numpy array to the console.
