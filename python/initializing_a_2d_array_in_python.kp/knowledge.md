---
title: What is the syntax for creating a two-dimensional array in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: A two-dimensional array can be initialized in Python by using the nested list syntax, i.e. arr = [[0 for x in range(cols)] for y in range(rows)].
---

**Contents**

[TOC]

# Section 1: Defining the Array

In Python, a two-dimensional array can be initialized by creating a list of lists. Each list within the list represents a row, and each element within the inner list represents a column.

# Section 2: Example

For example, the following code creates a two-dimensional array with 3 rows and 4 columns:

```
arr = [[0, 1, 2, 3], 
       [4, 5, 6, 7], 
       [8, 9, 10, 11]]
```

# Section 3: Accessing Elements

To access an element in the array, use the row and column index. For example, to access the element in the second row and third column, use the following syntax:

```
arr[1][2]  # returns 6
```

# Section 4: Iterating Over the Array

To iterate over the two-dimensional array, use two for loops. The outer loop will iterate over the rows, and the inner loop will iterate over the columns. For example:

```
for row in arr:
    for col in row:
        print(col)
```

This code will print each element in the array, one at a time.
