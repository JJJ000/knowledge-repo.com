---
title: What is the process of creating a numpy array using a generator?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Use np.fromiter() function to build a numpy array from a generator in Python.
---

**Contents**

[TOC]

## Introduction
One of the advantages of numpy over Python's built-in data structures is its ability to work with large numerical data. In some cases, the data may be too large to store in memory, which makes generators an appealing option. In this tutorial, we will explore how to build a numpy array from a generator in Python.

## Step 1: Generating Data
The first step is to create a generator that will yield the data. Here is an example of a generator that yields random numbers between 0 and 1:

```python
import random

def data_generator(n):
    for i in range(n):
        yield random.random()
```

The `data_generator` function takes an integer `n` as an argument, which specifies the number of elements to generate. It then uses a `for` loop to generate `n` random numbers using the `random.random()` function and yields each value.

## Step 2: Creating a numpy array
To create a numpy array from the generator, we can simply pass the generator to the `numpy.array()` method:

```python
import numpy as np

N = 10
data = np.array(data_generator(N))
```

In this example, we pass the `data_generator` function to `numpy.array()` along with the `N` value to generate 10 random numbers. The resulting `data` variable will be a numpy array with 10 elements.

## Step 3: Multiple Dimensional Arrays
If you want to build a multi-dimensional numpy array, you can modify the generator to yield tuples or lists of values, and then pass the generator to `numpy.array()` as before:

```python
import random

def data_generator(n):
    for i in range(n):
        yield (random.random(), random.random())

N = 3
data = np.array(list(data_generator(N)))
```

In this example, we use a generator that yields tuples of random numbers between 0 and 1. We then pass this generator to `numpy.array()` as before, but we need to wrap it in a `list()` function call to convert the generator to a list before creating the numpy array.

## Conclusion
In this tutorial, we explored how to build a numpy array from a generator in Python. We showed how to write a generator that generates random data, and how to pass it to `numpy.array()` to create a numpy array. We also demonstrated how to modify the generator to yield more complex data structures to create multi-dimensional numpy arrays.
