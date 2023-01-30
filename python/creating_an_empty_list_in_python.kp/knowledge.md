---
title: Create a list of a specified length in Python with no elements in it
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: You can create an empty list with a certain size in Python by using the list comprehension syntax [None]*size.
---

**Contents**

[TOC]

### Method 1: List Comprehension
Using list comprehension, an empty list with a certain size can be created as follows:

```
size = 5
empty_list = [None] * size
```

### Method 2: List Constructor
Using the list constructor, an empty list with a certain size can be created as follows:

```
size = 5
empty_list = list(None for _ in range(size))
```

### Method 3: Appending to List
Using the append method, an empty list with a certain size can be created as follows:

```
size = 5
empty_list = []
for _ in range(size):
    empty_list.append(None)
```

### Method 4: Using * Operator
Using the * operator, an empty list with a certain size can be created as follows:

```
size = 5
empty_list = [None] * size
```
