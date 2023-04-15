---
title: How to append a row to a numpy array?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: To add a row to an existing numpy array, use the numpy.vstack() function.
---

**Contents**

[TOC]

Section 1: Introduction to Numpy arrays
Numpy is a Python library used for working with arrays. Numpy is used extensively in data analysis and scientific computing. Numpy arrays are a type of data structure used for storing homogeneous data. They are similar to lists in Python, but they are faster and require less memory. 

Section 2: Adding a row to a Numpy array
To add a row to a Numpy array in Python, you can use the append() method. This method adds the elements of the row to the end of the array. Here is an example:

```python
import numpy as np

# creating a 2D Numpy array
arr = np.array([[1, 2, 3], 
              [4, 5, 6]])

# creating a row to append
row_to_add = np.array([7, 8, 9])

# appending the row to the array
arr = np.append(arr, [row_to_add], axis=0)

print("Updated array:")
print(arr)
```
Output:
```
Updated array:
[[1 2 3]
 [4 5 6]
 [7 8 9]]
```

Section 3: Understanding the code
In this code, we first import the Numpy library using the alias np. We then create a 2D Numpy array called arr containing 2 rows and 3 columns. We also create a row_to_add array containing three elements.

We then use the Numpy append() method to add the new row to the end of the array. The first argument to the append() method is the array we want to add the row to. The second argument is the row we want to add. The axis parameter specifies the axis along which we want to add the row. In this case, we want to add the row along the 0th axis, which represents the rows.

Finally, we print the updated array to the console.

Section 4: Conclusion
Adding a row to a Numpy array in Python is a simple process using the append() method. We can create a new row as a Numpy array and use the append() method to add it to the existing array. Numpy arrays are an essential tool for data analysis and scientific computing in Python.
