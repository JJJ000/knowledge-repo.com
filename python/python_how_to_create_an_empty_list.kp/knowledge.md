---
title: How to make a list with no elements in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: We can create an empty list in Python using empty bracket notation [].
---

**Contents**

[TOC]

Creating an empty list in Python

There are several ways to create an empty list in Python. Below are some ways explained:

1. Initializing an empty list using the List literal

One way to create an empty list in Python is to use the List literal and leave it empty. The List literal is simply a pair of square brackets that contains an optional comma-separated list of items.

```python
my_list = []
```

2. Using the list() constructor

Another way is to use the list() constructor to create an empty list. This constructor returns a new list and initializes it to be empty.

```python
my_list = list()
```

3. Using the copy() method

If you already have a list and want to create a new empty list with the same initial structure, you can use the copy() method. This method returns a new list with a shallow copy of the original list.

```python
my_list = [1, 2, 3]
new_list = my_list.copy()
new_list.clear()
```

4. Using the list comprehension

You can also create an empty list using a list comprehension. This technique is useful when you want to create a list with some specific structure or pattern.

```python
my_list = [i for i in range(0)]
```
