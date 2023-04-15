---
title: What is the syntax for finding the length of a list in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The number of elements in a list can be obtained by using the len() function.
---

**Contents**

[TOC]

# Using len()
The `len()` function can be used to get the length of a list in Python.

Syntax:
```
len(list)
```

Example:
```
list = [1, 2, 3, 4, 5]

len(list)

# Output: 5
```

# Iterating Through the List
Alternatively, you can iterate through the list and count the number of elements.

Syntax:
```
count = 0
for element in list:
    count += 1
```

Example:
```
list = [1, 2, 3, 4, 5]

count = 0
for element in list:
    count += 1

print(count)

# Output: 5
```
