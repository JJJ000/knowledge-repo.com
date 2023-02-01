---
title: Add values to a set in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: You can append values to a set in Python by using the set.add() method.
---

**Contents**

[TOC]

## Using the `add()` Method
The `add()` method can be used to append values to a set in Python. It takes one argument, which is the value to be added.

Example:
```
# Initialize a set
s = {1, 2, 3}

# Add a value
s.add(4)

# Print the set
print(s)
```
Output: `{1, 2, 3, 4}`

## Using the `update()` Method
The `update()` method can also be used to append values to a set in Python. It takes one argument, which is an iterable of values to be added.

Example:
```
# Initialize a set
s = {1, 2, 3}

# Add multiple values
s.update([4, 5, 6])

# Print the set
print(s)
```
Output: `{1, 2, 3, 4, 5, 6}`
