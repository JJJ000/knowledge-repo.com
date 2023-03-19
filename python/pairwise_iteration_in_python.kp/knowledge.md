---
title: Looping through every pair of consecutive elements in a list
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Use a for loop with a step of 2 to iterate over every two elements in a list in Python.
---

**Contents**

[TOC]

# Introduction
In some scenarios, we may want to iterate over a list in groups of two elements. This could be useful for comparing adjacent elements, pairing elements in a certain way, or performing operations that require information from two elements at a time. In this article, we will discuss different approaches to iterate over every two elements in a list in Python.

## Using a for loop with range and step
One way to iterate over every two elements in a list is using a for loop with range and step. Here is an example:

```python
my_list = [1, 2, 3, 4, 5, 6]
for i in range(0, len(my_list)-1, 2):
  print(my_list[i], my_list[i+1])
```

The output of this code will be:

```python
1 2
3 4
5 6
```

In this approach, we are using the range function to generate a sequence of indices, starting from 0 and incrementing by 2 until len(my_list)-1. During each iteration of the for loop, we access my_list[i] and my_list[i+1] to get the pairs of elements.

## Using zip and slicing
Another approach to iterate over every two elements in a list is by using the zip function with slicing. Here is an example:

```python
my_list = [1, 2, 3, 4, 5, 6]
for x, y in zip(my_list[::2], my_list[1::2]):
  print(x, y)
```

The output of this code will be:

```python
1 2
3 4
5 6
```

In this approach, we are using slicing to extract every second element of the list, starting from index 0 and 1, then using zip to pair corresponding elements into tuples. During each iteration of the for loop, we unpack these tuples into x and y variables.

## Using pairwise function from itertools module
Another easy way to iterate over every two elements in a list is to use the pairwise function from the itertools module. Here is an example:

```python
from itertools import tee

def pairwise(iterable):
    a, b = tee(iterable)
    next(b, None)
    return zip(a, b)

my_list = [1, 2, 3, 4, 5, 6]
for x, y in pairwise(my_list):
  print(x, y)
```

The output of this code will be:

```python
1 2
2 3
3 4
4 5
5 6
```

In this approach, we define a pairwise function that takes an iterable as input and returns a generator that yields pairs of adjacent elements. The function uses the tee function to create two copies of the iterable, advances the second copy by one element using next(b, None), and returns a zip() of the two copies. 

## Conclusion
These are some of the different approaches to iterate over every two elements in a list in Python. Depending on the specific use case, one approach may be more appropriate than others in terms of readability, performance, or flexibility. Hopefully, this article helps you choose the best approach for your problem.
