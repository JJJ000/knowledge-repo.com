---
title: What is the method of numerically sorting a list of strings?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Use the sorted() function with the key parameter set to int.
---

**Contents**

[TOC]

## Convert strings to numbers

The first step to numerically sort a list of strings in Python is to convert the strings to numbers. This can be done using functions such as `int()` or `float()` depending on the type of numbers in the strings. 

For example, consider the following list of strings:

```
nums = ["10", "23", "5", "8", "15"]
```

To convert these strings to integers, we can use a for loop and the `int()` function:

```python
nums_int = []

for num in nums:
    nums_int.append(int(num))
```

The resulting list `nums_int` will contain integers:

```
[10, 23, 5, 8, 15]
```

## Sort the list

Once the list of strings has been converted to a list of numbers, we can use the `sort()` method to sort the list numerically. 

```python
nums_int.sort()
```

This will sort the list `nums_int` in ascending order:

```
[5, 8, 10, 15, 23]
```

If we want to sort the list in descending order, we can use the `reverse` parameter:

```python
nums_int.sort(reverse=True)
```

This will sort the list in descending order:

```
[23, 15, 10, 8, 5]
```

## One-liner solution

It is possible to sort a list of strings numerically in Python using a one-liner solution:

```python
nums = ["10", "23", "5", "8", "15"]
nums_sorted = sorted(map(int, nums))
```

The `map()` function is used to convert the strings to integers, and the `sorted()` function is used to sort the resulting list of integers. This will produce the same result as the previous example:

```
[5, 8, 10, 15, 23]
```
