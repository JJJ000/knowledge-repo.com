---
title: How to obtain the count of elements in a Python iterator?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use the `len()` function to get the number of elements in an iterator in Python.
---

**Contents**

[TOC]

## Using the `len()` function

One simple and effective way to get the number of elements in an iterator in Python is to use the built-in `len()` function. This function takes an iterable as its argument and returns the number of items it contains. Here's an example:

```python
my_list = [1, 2, 3, 4, 5]
my_tuple = (6, 7, 8, 9, 10)
my_iterator = iter(range(11, 16))

print(len(my_list))      # output: 5
print(len(my_tuple))     # output: 5
print(len(my_iterator))  # output: 5
```

In this example, we use three different data structures (`list`, `tuple`, and `range` object) to create three different iterables. We pass each of these iterables as arguments to the `len()` function and the function returns the number of items in each iterable.

## Using a loop to count the elements

Another way to get the number of elements in an iterator is to loop through it and count the number of times the loop is executed. Here's an example using the `list` data structure:

```python
my_list = [1, 2, 3, 4, 5]
count = 0

for element in my_list:
    count += 1

print(count)  # output: 5
```

In this example, we create a `list` and initialize a counter to zero. We then use a `for` loop to iterate over each element in the list and increment the counter by one for each element. Once the loop has completed, the counter contains the number of elements in the list.

## Using `sum()` with a generator expression

If we have a large amount of data in the iterator and want to avoid loading everything into memory, we can use the `sum()` function with a generator expression to count the number of elements. A generator expression creates a generator object on the fly that produces values as they are needed, allowing us to iterate over large amounts of data without loading everything into memory. Here's an example:

```python
my_iterator = iter(range(1000000))
count = sum(1 for _ in my_iterator)

print(count)  # output: 1000000
```

In this example, we create an iterator object that generates one million consecutive integers. We then use a generator expression (`1 for _ in my_iterator`) to create a series of `1`s, one for each item in the iterator, and pass the resulting generator object as an argument to the `sum()` function. The `sum()` function adds up all the values produced by the generator, which in this case is one million, giving us the number of elements in the original iterator.

## Using itertools module

Similar to the previous example one can achieve more performance effective way with `itertools`. Specifically, `itertools.accumulate` with the argument `func=lambda x,y: x+1` can be used: 

```python
import itertools

my_iterator = iter(range(1000000))
count = next(itertools.accumulate(my_iterator, func=lambda x,y: x+1))

print(count)  # output: 1000000
```

In this example, we create an iterator object that generates one million consecutive integers. We then use the `itertools.accumulate` function and provide a function that sums each consecutive pair with one. As the name suggests `itertools.accumulate` produces an iterator that accumulates the output giving, in the end, the number of elements. The `next` function is used to get the value of the accumulated iterator.
