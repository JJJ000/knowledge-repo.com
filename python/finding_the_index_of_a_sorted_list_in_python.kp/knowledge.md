---
title: What is the method of obtaining the index of a sorted list?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Use the index() function to return the index of a specific element in a sorted list.
---

**Contents**

[TOC]

# Sorting a list in Python
To sort a list in Python, you can use the `sorted()` function. This function takes an iterable (e.g. a list) and returns a new sorted list, leaving the original list unchanged.

```python
my_list = [3, 1, 4, 1, 5, 9, 2, 6, 5, 3]
sorted_list = sorted(my_list)
print(sorted_list)
# Output: [1, 1, 2, 3, 3, 4, 5, 5, 6, 9]
```

# Returning index of a value in a list
To return the index of a value in a list, you can use the `index()` method. This method takes a value and returns the index of the first occurrence of that value in the list. If the value is not found, a `ValueError` exception is raised.

```python
my_list = [3, 1, 4, 1, 5, 9, 2, 6, 5, 3]
index_of_2 = my_list.index(2)
print(index_of_2)
# Output: 6
```

# Returning index of a value in a sorted list
To return the index of a value in a sorted list, you can use the `bisect()` function from the `bisect` module. This function takes a sorted list and a value, and returns the index where the value should be inserted to maintain the sorted order.

```python
import bisect

sorted_list = [1, 1, 2, 3, 3, 4, 5, 5, 6, 9]
index_of_2 = bisect.bisect_left(sorted_list, 2)
print(index_of_2)
# Output: 2
```

Note that `bisect_left()` is used instead of `bisect()` to return the index of the leftmost occurrence of the value, if there are multiple occurrences. If you want the index of the rightmost occurrence, you can use `bisect_right()` instead.
