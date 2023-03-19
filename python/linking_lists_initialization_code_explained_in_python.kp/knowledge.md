---
title: How come this code, which initializes a list of lists, seems to interconnect the lists?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: The code links the lists together because each sublist is actually a reference to the same object in memory, created by repeating the same empty list object n times.
---

**Contents**

[TOC]

## Explanation of Code

The code initializes a list of lists in Python using the repetition operator (`*`) and the `list()` constructor. It looks like this:

```
matrix = [[0] * 3] * 3
```

This creates a 3x3 matrix (list of lists), with each "sub-list" initialized to `[0, 0, 0]`. 

## Reference Semantics in Python

Python uses **reference semantics**, which means that variables don't actually "contain" values; they refer to (or "point to") objects in memory. When we create a list object, Python creates an object in memory and assigns a reference to that object to our variable.

In our case, we're creating a list (`[0, 0, 0]`) and then using the repetition operator to create three references to the same list object. We're then adding those references to another list (our matrix).

```
matrix = [[0] * 3] * 3
         |   |     |___|
         |   |       |
         |   |       | Reference to same list
         |   |
         |   | Reference to same list
         |
         | Reference to same list
```

## The Mutable Nature of Lists

In Python, lists are mutable objects. This means that we can change the values in a list, even after it's been created. However, because all of the sub-lists in our matrix are actually references to the same list object, any changes we make to one of them will affect all of them.

```
matrix = [[0] * 3] * 3
matrix[0][0] = 1

print(matrix)
# Output: [[1, 0, 0], [1, 0, 0], [1, 0, 0]]
```

Here, we're changing the value at `[0][0]` in our matrix to `1`. However, because all of the sub-lists in the matrix are actually references to the same list object, this change is reflected in every sub-list, not just the one we intended to change.

## Avoiding this Behavior

To avoid this behavior, we need to create new list objects for each sub-list in our matrix, rather than simply creating new references to the same list object. One way to do this is to use a list comprehension:

```
matrix = [[0 for j in range(3)] for i in range(3)]
```

This creates a new list object for each sub-list in our matrix, so that changes made to one sub-list won't affect the others. 

```
matrix = [[0 for j in range(3)] for i in range(3)]
matrix[0][0] = 1

print(matrix)
# Output: [[1, 0, 0], [0, 0, 0], [0, 0, 0]]
```
