---
title: Locating the position of an element in a list
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-08 00:00:00
updated_at: 2023-01-08 00:00:00
tldr: Use the `list.index(item)` method to find the index of an item in a list in Python.
---

**Contents**

[TOC]

### Using the Index Method
The index method can be used to find the index of an item in a list. To do this, simply pass the item you are searching for as an argument to the index method.

Example:
```python
my_list = [1, 2, 3, 4]

# Find the index of the number 3
my_list.index(3)
```
Output:
```python
2
```

### Using a For Loop
A for loop can also be used to find the index of an item in a list. To do this, loop through the list and compare each item to the item you are searching for.

Example:
```python
my_list = [1, 2, 3, 4]

# Find the index of the number 3
for i in range(len(my_list)):
    if my_list[i] == 3:
        print(i)
```
Output:
```python
2
```
