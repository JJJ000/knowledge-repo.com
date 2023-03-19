---
title: What is the procedure for arranging a counter in Python based on its value?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: You can sort a Counter in Python by value using the method `most\_common()` with the parameter `reverse=True`.
---

**Contents**

[TOC]

## Obtaining a Counter object

To sort a Counter by value, we first need a Counter object. We can create a Counter using the built-in Python class `collections.Counter`. Here is an example of how to create a Counter object:

```python
from collections import Counter
my_list = [1,2,3,2,1,3,1,1,2,2,2]
c = Counter(my_list)
```

In this example, we first import the `Counter` class from the `collections` module. Then we create a list of integers (`my_list`) and pass it to the `Counter` constructor to create a Counter object `c`. 

## Getting a sorted list of Counter items

Once we have a Counter object, we can use the `most_common()` method to get a list of items sorted by frequency:

```python
sorted_list = c.most_common()
```

By default, `most_common()` returns a list of tuples where each tuple contains an item from the Counter and its frequency. The list is sorted in descending order of frequency. 

## Sorting a list of Counter items by value

To sort the list of Counter items by value instead of frequency, we can use the `key` parameter of the `sorted()` function. We pass a lambda function to the `key` parameter that extracts the second element of the tuple (i.e. the count) and uses it as the sort key:

```python
sorted_list_by_value = sorted(c.items(), key=lambda x: x[1])
```

In this example, we use the `items()` method of the Counter object to get a list of tuples where each tuple contains an item from the Counter and its count. We pass this list to the `sorted()` function along with a lambda function that extracts the count (i.e. the second element of each tuple) and uses it as the sort key. The resulting list (`sorted_list_by_value`) is sorted in ascending order of value. 

## Alternative method using the Counter.most_common() method

Alternatively, we can use the `most_common()` method with a small twist. We instead, reverse the list so that now the elements are sorted by their value. Here is how:

```python
sorted_list_by_value = c.most_common()[::-1]
```

Here, beyond simply reversing the list, the `most_common()` method, by default (when no parameter passed), sorts the most common elements by their count (which we want to reverse i.e. sort by the value).
