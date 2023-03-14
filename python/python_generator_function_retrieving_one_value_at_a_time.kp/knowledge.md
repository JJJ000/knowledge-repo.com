---
title: What is the way to fetch a single value at a time from a generator function in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Use the next() function to get one value at a time from a generator function in Python.
---

**Contents**

[TOC]

# Understanding Generator Functions 

Generator functions in Python are special functions that act as iterators to help us loop through sequences very efficiently. 
A generator function yields values one at a time instead of returning all the values at once, which helps save memory and improve performance. 

Here's an example of a generator function:
```python
def my_generator():
    yield 1
    yield 2
    yield 3
```

In this case, when `my_generator()` is called, it returns an iterator object. Every time we use the `next()` function on our iterator object, the generator function is executed to produce the next value from the sequence.

# Using the next() function

To get one value at a time from a generator function, we can use the built-in `next()` function.
We can use `next()` to obtain the values from the generator function until there are no more values to be yielded. 

Here's an example:
```python
def my_generator():
    yield 1
    yield 2
    yield 3

# creating an iterator object
itr = my_generator()

# getting one value at a time using next()
val = next(itr)
print(val)  # outputs: 1

val = next(itr)
print(val)  # outputs: 2

val = next(itr)
print(val)  # outputs: 3

# when there are no more values to be yielded, a StopIteration exception is raised
val = next(itr)   # raises: StopIteration
```

Using the `next()` function, we can get the values one at a time from a generator function until we get a `StopIteration` exception. 


# Using loops to get values from generator functions

Another way to get values from a generator function in Python is to use a `for` loop. 
In this case, we don't need to explicitly call the `next()` function. The loop automatically calls `next()` behind the scenes, and stops when the generator function raises a `StopIteration` exception.

Here's an example:
```python
def my_generator():
    yield 1
    yield 2
    yield 3 

# using a for loop to fetch values from the generator function
for val in my_generator():
    print(val)
# outputs:
# 1
# 2
# 3
```

Using a `for` loop, we can fetch all the values from a generator function one at a time without running into any `StopIteration` exception.

# Conclusion
Generator functions in Python are powerful tools that allow us to efficiently work with sequences of data, particularly when dealing with large datasets. By using the `next()` function or a `for` loop, we can obtain the values from the generator function one at a time or in batches without having to store all the values in memory.
