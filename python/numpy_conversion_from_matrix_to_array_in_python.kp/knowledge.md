---
title: Transforming a numpy matrix into an array
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Use the `.flatten()` method to convert a numpy matrix to a one-dimensional array in Python.
---

**Contents**

[TOC]

Section 1: Understanding Numpy
Numpy is a Python library used for numerical operation. It provides an array object which is similar to the array object in the Matlab software. Numpy arrays are homogeneous arrays of fixed-size unlike Python lists which are heterogeneous arrays of variable sized.

Section 2: Converting Numpy Matrix to Array
Numpy arrays can be created from Python lists or tuples. In the same way, we can convert a numpy matrix to an array using the `np.asarray()` method. 

The conversion from matrix to array can be easily done as shown in the code below:

```
import numpy as np

matrix = np.matrix('1 2 3; 4 5 6; 7 8 9')
array = np.asarray(matrix)
```

In this example code, we first create a numpy matrix of size 3x3. Then, we use the `np.asarray()` method to convert the matrix to an array object. The resulting object is an array object with the same contents as the input matrix.

Section 3: Example
In this example, we are going to create a numpy matrix and then convert it to an array.

```
import numpy as np

matrix = np.matrix('2 4 6; 8 10 12')
array = np.asarray(matrix)

print("Input Matrix:\n", matrix)
print("Output Array:\n", array)
```

In the above code, we create a matrix with dimensions 2x3. Then, we use the `np.asarray()` method to convert the matrix to an array. The output is printed to the console as shown below:

```
Input Matrix:
 [[ 2  4  6]
 [ 8 10 12]]
Output Array:
 [[ 2  4  6]
 [ 8 10 12]]
```

Section 4: Conclusion
In this tutorial, we have seen how to convert a numpy matrix to an array in Python using the `np.asarray()` method. This method is a simple way to convert a matrix object to an array object in numpy.
