---
title: What is the process of extracting individual lists from a compressed list of tuples?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Use the zip function and the asterisk operator, like this list\_1, list\_2 = zip(*list\_of\_tuples).
---

**Contents**

[TOC]

### Section 1: Unzipping a single tuple

The `zip()` function in Python is used to take two or more iterables and return a `zip` object, which is an iterator of tuples where the first item in each passed iterable is paired together, and then the second item in each passed iterable is paired together, and so on.

To unzip a single tuple into individual lists, we can use the `zip()` function again in combination with the `*` operator:

```python
my_tuple = (1, 2, 3)
list1, list2, list3 = zip(*my_tuple)
```

### Section 2: Unzipping a list of tuples with equal length

To unzip a list of tuples into individual lists, where each tuple has the same length, we can use a list comprehension in combination with the `zip()` function and the `*` operator:

```python
my_list_of_tuples = [(1, 2), (3, 4), (5, 6)]
list1, list2 = [list(i) for i in zip(*my_list_of_tuples)]
```

### Section 3: Unzipping a list of tuples with unequal length

If the tuples in the list have unequal length, we can use the `itertools.zip_longest()` function instead of the built-in `zip()` function. This function takes two or more iterables as arguments and returns an iterator that aggregates elements from each iterable based on the longest iterable.

We can then use a list comprehension to iterate over the resulting iterator and collect the values into individual lists:

```python
import itertools

my_list_of_tuples = [(1, 2), (3,), (4, 5, 6)]
list1, list2, list3 = [list(i) for i in itertools.zip_longest(*my_list_of_tuples, fillvalue=None)]
```

### Section 4: Conclusion

Unzipping a list of tuples into individual lists can be achieved using the built-in `zip()` function and the `*` operator. However, if the tuples have unequal length, we should use the `itertools.zip_longest()` function instead.
