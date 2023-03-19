---
title: Using a list of indexes, numpy can select a particular column index for each row
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-15 00:00:00
updated_at: 2023-03-15 00:00:00
tldr: To select specific columns per row using a list of indexes in NumPy, use the syntax array\_name[, [list\_of\_indexes]].
---

**Contents**

[TOC]

Section 1: Introduction to the problem

NumPy is a commonly used library for numerical computing in Python. One of the common operations in data analysis is selecting specific column index per row by using a list of indexes. In this task, we will explore how to achieve this by using NumPy library in Python.

Section 2: Creating a NumPy array

First, let's create a NumPy array to work with. We will create an array of 5 rows and 4 columns:

```python
import numpy as np

# Create a 5x4 numpy array
arr = np.array([[1, 2, 3, 4],
                [5, 6, 7, 8],
                [9, 10, 11, 12],
                [13, 14, 15, 16],
                [17, 18, 19, 20]])

```

Section 3: Selecting specific column index per row using a list of indexes

Now, let's say we want to select the 1st, 3rd, and 4th column indexes for rows 1, 2, and 4. We can achieve this by using NumPy's advanced indexing feature:

```python
# Select columns 1, 3, and 4 for rows 1, 2, and 4
rows = np.array([1, 2, 4])
cols = np.array([0, 2, 3])

selected = arr[rows[:, np.newaxis], cols]

print(selected)
```

Output:
```
[[ 5  7  8]
 [ 9 11 12]
 [17 19 20]]
```

Here, we first create two NumPy arrays `rows` and `cols`, which contain the row and column indexes we want to select. We then use the `np.newaxis` attribute to convert `rows` into a column vector, which allows us to use it with the column indexes in `cols`. Finally, we use the advanced indexing feature of NumPy to select the specified rows and columns, and store the result in the variable `selected`.

Section 4: Conclusion

In this task, we have explored how to select specific column index per row by using a list of indexes in NumPy. We have used NumPy's advanced indexing feature to achieve this, and also demonstrated how to create a NumPy array to work with. This technique can be very useful in data analysis and for operations requiring row and column indices.
