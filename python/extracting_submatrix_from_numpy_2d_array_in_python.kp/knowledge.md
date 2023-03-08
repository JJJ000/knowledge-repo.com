---
title: How can I extract an mxm submatrix from an nxn array (where n is greater than m) using numpy's array slicing method?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: To extract an mxm submatrix from an nxn NumPy array, you can use slicing with array[0m, 0m].
---

**Contents**

[TOC]

# Section 1: Introduction

Slicing is a way of extracting a portion of a NumPy array. In this case, we want to extract an mxm submatrix from an nxn array, where n>m. In this article, we will go through the steps to extract a submatrix of an mxm size from an nxn array.


# Section 2: Extracting an mxm Submatrix

There are several ways to extract an mxm submatrix from an nxn array. One way is to use the slicing feature of NumPy.


```python
import numpy as np

# Create an nxn array
n = 6
arr_nxn = np.arange(n**2).reshape(n, n)

# Extract an mxm submatrix from the nxn array
m = 3
arr_mxm = arr_nxn[:m, :m]

# Print the submatrix
print('Submatrix:\n', arr_mxm)
```

The output will be:

```
Submatrix:
 [[ 0  1  2]
  [ 6  7  8]
  [12 13 14]]
```

In this example, we created an nxn array using NumPy's `arange` function and then reshaped it to an nxn matrix using the `reshape` function. We then extracted an mxm submatrix from the nxn array by taking the first m rows and columns using the slicing operator `:`. The resulting submatrix is of size mxm.


# Section 3: Using Integer Indexing

Another way to extract an mxm submatrix from an nxn array is to use integer indexing.


```python
# Create an nxn array
n = 6
arr_nxn = np.arange(n**2).reshape(n, n)

# Extract an mxm submatrix from the nxn array
m = 3
arr_mxm = arr_nxn[:m, :m]

# Print the submatrix using integer indexing
print('Submatrix:\n', arr_nxn[np.ix_(range(m), range(m))])
```

The output will be the same as in Section 2:

```
Submatrix:
 [[ 0  1  2]
  [ 6  7  8]
  [12 13 14]]
```

In this example, we used NumPy's `ix_` function to create an index array of size mx2 (where m is the size of the submatrix). We then used this index array to extract the submatrix from the nxn array.


# Section 4: Conclusion

In this article, we learned two ways to extract an mxm submatrix from an nxn array in Python using NumPy. The slicing operator and integer indexing can be used to achieve this task.
