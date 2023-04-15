---
title: What is the procedure for obtaining the length of generator()?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can get the length of a generator in Python using the built-in function `sum(1 for \_ in generator())` which returns the number of items in the generator.
---

**Contents**

[TOC]

## Overview
Python generators are special functions that allow us to iterate over a sequence of values without actually creating the entire sequence at once. This makes them efficient for working with large datasets. However, it also means that traditional methods for finding the length of a sequence, such as using the `len()` function, don't work. 

In this guide, we'll explore a few different methods for finding the length of a generator object in Python. 

## Method 1: Converting to a List
One simple way to find the length of a generator object is to convert it to a list using the `list()` function, and then find the length of the resulting list using `len()`. Here's an example:

```python
my_gen = (x**2 for x in range(10))  # create a generator of squares
my_list = list(my_gen)  # convert generator to a list
print(len(my_list))  # output: 10
```

This works, but it can be inefficient for very large datasets, since it requires loading the entire sequence into memory at once. 

## Method 2: Iterating and Counting
Another approach is to iterate over the generator object and manually count the number of elements. Here's an example:

```python
my_gen = (x**2 for x in range(10))  # create a generator of squares
count = 0
for _ in my_gen:
    count += 1
print(count)  # output: 10
```

This method is more efficient than converting to a list, since it only requires storing a single integer in memory. However, it's worth noting that once the generator has been fully iterated over, it can't be used again (i.e. you can't call `len()` or iterate over it again). 

## Method 3: Using the itertools module
The `itertools` module in Python provides a number of tools for working with iterators and generators. One of these is the `tee()` function, which can be used to create multiple identical copies of an iterator or generator. We can then use one copy to iterate over the sequence and count the number of elements, while leaving the other copy untouched (in case we need to use it again later). Here's an example:

```python
import itertools

my_gen = (x**2 for x in range(10))  # create a generator of squares
my_gen, copy = itertools.tee(my_gen)  # create two identical copies of the generator
count = sum(1 for _ in my_gen)  # iterate over one copy and count the elements
print(count)  # output: 10
```

This method is similar to the previous one, but it allows us to preserve the original generator object (in case we need to use it again later). However, it does require importing a module, which may not be desirable in all situations. 

## Conclusion
In summary, there are multiple ways to find the length of a generator object in Python. The best method will depend on the specific situation and the size of the dataset being processed. The first method (converting to a list) is simple but inefficient for large datasets, while the second method (iterating and counting) is more efficient but can only be used once. The third method (using the `itertools` module) is a good compromise, since it allows us to preserve the original generator object while still being efficient.
