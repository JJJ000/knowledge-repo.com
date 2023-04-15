---
title: How to append an element to a Python tuple?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: It is not possible to add items to a tuple as it is an immutable data type in Python.
---

**Contents**

[TOC]

## Creating a tuple

To add an item to a tuple, we first need to create a tuple. A tuple is a collection of ordered, immutable elements enclosed in parentheses. 

```python
# creating a tuple
tuple_1 = (1, 2, 3, 4)
```

## Converting tuple into a list

Since tuples are immutable, we cannot add or remove any elements from them. Thus, before we can add an item to the tuple, we must first convert it into a list.

```python
# converting tuple into list
list_1 = list(tuple_1)
``` 

## Adding item to the list 

Once we have the list, we can add new elements to it using various methods. In this example, we use the `append()` function to add a new item to the end of the list.

```python
# adding item to the list
list_1.append(5)
```

## Converting list back to tuple

Finally, after adding the item to the list, we need to convert it back to a tuple using the `tuple()` function.

```python
# converting list back to tuple
tuple_2 = tuple(list_1)
``` 

Now `tuple_2` will have the new item added to it.
