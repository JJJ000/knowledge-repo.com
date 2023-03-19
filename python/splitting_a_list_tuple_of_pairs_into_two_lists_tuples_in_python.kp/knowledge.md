---
title: Converting a list/tuple of pairs into two separate lists/tuples
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use `zip(*list\_of\_pairs)` to unpack a list/tuple of pairs into two separate lists/tuples.
---

**Contents**

[TOC]

Introduction

Python provides a handy way of packing and unpacking values using tuples. You can use tuple unpacking to map two lists into a dictionary, you can use it to swap the values of two variables without using a temporary variable, and you can also use it to unpack a list/tuple of pairs into two separate lists/tuples.

Unpacking a list/tuple of pairs into two lists/tuples can be useful in many situations, such as when you have a list of (x, y) points and you need to plot them separately, or when you have a list of key-value pairs and you need to extract the keys and values separately.

In this article, we will learn how to unpack a list/tuple of pairs into two lists/tuples in Python.

Method 1: Using a loop

The simplest way to unpack a list/tuple of pairs into two lists/tuples is to use a loop. Here's a code example:

```python
pairs = [(1, 'a'), (2, 'b'), (3, 'c')]

xs = []
ys = []

for x, y in pairs:
    xs.append(x)
    ys.append(y)

print(xs) # [1, 2, 3]
print(ys) # ['a', 'b', 'c']
```

In this example, we define a list of (x, y) pairs and then initialize two empty lists (xs and ys). We then loop over each pair in the list using tuple unpacking and append the x values to the xs list and the y values to the ys list.

Using a loop to unpack a list/tuple of pairs is simple and easy to understand, but it can be inefficient for large lists.

Method 2: Using zip and the * operator

A more efficient way to unpack a list/tuple of pairs into two lists/tuples is to use the zip function and the * operator. Here's a code example:

```python
pairs = [(1, 'a'), (2, 'b'), (3, 'c')]

xs, ys = zip(*pairs)

print(xs) # (1, 2, 3)
print(ys) # ('a', 'b', 'c')
```

In this example, we define a list of (x, y) pairs and use the zip function and the * operator to unpack the pairs into two separate tuples (xs and ys).

The zip function takes multiple iterable inputs and returns an iterator of tuples where the i-th tuple contains the i-th element from each of the input iterables.

By using the * operator on the pairs list, we effectively unpack the list of pairs into two separate arguments that are passed to the zip function. The zip function then returns two tuples that we can assign to the xs and ys variables.

Using the zip function and the * operator to unpack a list/tuple of pairs is more efficient than using a loop, especially for large lists.

Conclusion

Unpacking a list/tuple of pairs into two separate lists/tuples is a common operation in Python programming. We have learned two methods to do this: using a loop and using the zip function and the * operator. While both methods produce the same result, using the zip function and the * operator is generally more efficient, especially for large lists.
