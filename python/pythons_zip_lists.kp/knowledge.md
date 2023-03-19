---
title: Rearrange the lists in Python using the zip function
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Zip lists in Python creates an iterator that aggregates the elements from two or more iterables by iterating through them in a parallel fashion.
---

**Contents**

[TOC]

Section 1: Introduction to Zip Lists
-------------------------------------

Zip function is a built-in function in python's standard library. It is a convenient and powerful tool for aggregating, combining, or matching data from multiple lists.

In python, a zip object is created by calling the built-in zip function. This object can be iterated over to produce tuples containing elements from each of the input lists.

Several examples of operations that can be performed with zip lists in python include creating dictionaries from two lists, generating pairs of elements from two or more lists, and transposing rows and columns of a matrix.

Section 2. Creation of zip lists
----------------------------------

The zip function can be used to aggregate any number of lists, sequences, or iterators. To create a zip object, we pass the input sequences as positional arguments to the zip function.

Here's a sample code that demonstrates creating a zip object from two lists:

```
x = [1, 2, 3]
y = [4, 5, 6]
z = zip(x, y)
```
After executing this code, the variable `z` will contain a zip object that can be iterated over to produce tuples `(1, 4)`, `(2, 5)`, and `(3, 6)`.

Section 3. Unzipping and zipping a list
----------------------------------------

To extract the individual sequences from a zip object, we can use the `*` operator to unpack the tuples. Here's a sample code that demonstrates how to unzip a zip object:

```python
x, y = zip(*z)
```

Here, the `*` operator is used to unpack the tuples produced by iterating over the zip object `z`. The variables `x` and `y` will now contain the sequences `[1, 2, 3]` and `[4, 5, 6]`, respectively.

Conversely, to create a zip object from sequences that are already stored in variables, we can use the `zip` function in a similar way. Here's a sample code that demonstrates zipping two lists:

```python
x = [1, 2, 3]
y = [4, 5, 6]
z = zip(x, y)
```

Section 4. Zipping uneven sequences
-----------------------------------

If the input sequences to the zip function have different lengths, the resulting zip object will be truncated to the length of the shortest sequence. For example, if we try to zip two lists with three elements and four elements, respectively, the resulting zip object will have three tuples.

Here's a sample code that demonstrates this behavior:

```python
x = [1, 2, 3]
y = [4, 5, 6, 7]
z = zip(x, y)
```

After executing this code, the variable `z` will contain a zip object that can be iterated over to produce tuples `(1, 4)`, `(2, 5)`, and `(3, 6)`. The last element `7` is not included in the zip object because the length of the `x` sequence is 3.
