---
title: What is the process for clearing a list?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: To empty a list in Python, set it equal to an empty list, e.g. my\_list = []
---

**Contents**

[TOC]

#1 Using a Loop

This approach involves iterating through the list and reassigning each item to an empty value.

```python
my_list = [1, 2, 3, 4]

for i in range(len(my_list)):
    my_list[i] = []

print(my_list) # Output: [[], [], [], []]
```

#2 Using the Clear Method

The `clear()` method can be used to empty a list.

```python
my_list = [1, 2, 3, 4]

my_list.clear()

print(my_list) # Output: []
```

#3 Reassigning the Variable

This approach involves reassigning the list variable to a new empty list.

```python
my_list = [1, 2, 3, 4]

my_list = []

print(my_list) # Output: []
```

#4 Using the del Statement

The `del` statement can be used to remove items from a list or clear the entire list.

```python
my_list = [1, 2, 3, 4]

del my_list[:]

print(my_list) # Output: []
```
