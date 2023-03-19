---
title: Transform a tuple into a list and then revert it back to its original form
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: To convert tuple to list in Python, use the list() method, and to convert a list back to a tuple, use the tuple() method.
---

**Contents**

[TOC]

## Converting a tuple to a list

To convert a tuple to a list in Python, we can use the `list()` function. Here's an example:

```python
my_tuple = (1, 2, 3)
my_list = list(my_tuple)
print(my_list) # Output: [1, 2, 3]
```

In this code, we first declare a tuple `my_tuple` with three elements. Then, we use the `list()` function to create a new list `my_list` from the tuple. Finally, we print the resulting list to the console.

## Converting a list to a tuple

To convert a list to a tuple in Python, we can use the `tuple()` function. Here's an example:

```python
my_list = [1, 2, 3]
my_tuple = tuple(my_list)
print(my_tuple) # Output: (1, 2, 3)
```

In this code, we first declare a list `my_list` with three elements. Then, we use the `tuple()` function to create a new tuple `my_tuple` from the list. Finally, we print the resulting tuple to the console.

## Converting a nested tuple to a nested list

To convert a nested tuple to a nested list in Python, we can use a combination of the `list()` function and list comprehension. Here's an example:

```python
my_nested_tuple = ((1, 2), (3, 4))
my_nested_list = [list(x) for x in my_nested_tuple]
print(my_nested_list) # Output: [[1, 2], [3, 4]]
```

In this code, we first declare a nested tuple `my_nested_tuple` with two tuples as its elements. Then, we use list comprehension to apply the `list()` function to each nested tuple, creating a nested list `my_nested_list`. Finally, we print the resulting nested list to the console.

## Converting a nested list to a nested tuple

To convert a nested list to a nested tuple in Python, we can use a combination of the `tuple()` function and list comprehension. Here's an example:

```python
my_nested_list = [[1, 2], [3, 4]]
my_nested_tuple = tuple(tuple(x) for x in my_nested_list)
print(my_nested_tuple) # Output: ((1, 2), (3, 4))
```

In this code, we first declare a nested list `my_nested_list` with two lists as its elements. Then, we use list comprehension to apply the `tuple()` function to each nested list, creating a nested tuple `my_nested_tuple`. Finally, we print the resulting nested tuple to the console.
