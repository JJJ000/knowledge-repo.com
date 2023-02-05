---
title: Switch the position of the elements in each list
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: To transpose a list of lists in Python, use the zip() function to unpack the list of lists, followed by the star operator (*) to unpack the zip object into individual arguments for the list() constructor.
---

**Contents**

[TOC]

### Solution 1: Using Zip

We can use the `zip` built-in function to transpose a list of lists in Python. The `zip` function takes two or more iterables and creates an iterator of tuples, where the first item in each passed iterator is paired together, and then the second item in each passed iterator are paired together, and so on. 

```python
list_of_lists = [[1,2,3], [4,5,6], [7,8,9]]

transposed = list(zip(*list_of_lists))

print(transposed)
# Output: [(1, 4, 7), (2, 5, 8), (3, 6, 9)]
```

### Solution 2: Using Nested List Comprehension

We can also use nested list comprehension to transpose a list of lists in Python. A nested list comprehension is a list comprehension inside another list comprehension which is quite similar to nested for loops.

```python
list_of_lists = [[1,2,3], [4,5,6], [7,8,9]]

transposed = [[row[i] for row in list_of_lists] for i in range(len(list_of_lists[0]))]

print(transposed)
# Output: [[1, 4, 7], [2, 5, 8], [3, 6, 9]]
```

### Solution 3: Using Numpy

We can also use the `numpy` module to transpose a list of lists in Python. The `numpy` module provides a `transpose` function which can be used to transpose a given matrix.

```python
import numpy as np

list_of_lists = [[1,2,3], [4,5,6], [7,8,9]]

transposed = np.transpose(list_of_lists)

print(transposed)
# Output: [[1 4 7]
#          [2 5 8]
#          [3 6 9]]
```

### Solution 4: Using For Loops

We can also use for loops to transpose a list of lists in Python. This approach involves two for loops, one nested inside the other. The outer loop iterates through each row of the given matrix and the inner loop iterates through each element of the row.

```python
list_of_lists = [[1,2,3], [4,5,6], [7,8,9]]

transposed = []
for i in range(len(list_of_lists[0])):
    new_row = []
    for row in list_of_lists:
        new_row.append(row[i])
    transposed.append(new_row)

print(transposed)
# Output: [[1, 4, 7], [2, 5, 8], [3, 6, 9]]
```
