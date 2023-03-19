---
title: How to perform a transpose of a matrix in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: In Python, matrix transpose can be obtained by using the numpy.transpose() function.
---

**Contents**

[TOC]

What is Matrix Transpose?
------------------------
Matrix transpose is an operation in which the rows and columns of a given matrix are interchanged. In other words, the matrix is flipped over its diagonal.


Using Numpy to Transpose Matrix in Python
-----------------------------------------
Numpy is a popular library for scientific computing in Python. It provides a convenient way to perform various operations on matrices, including matrix transpose. Here's how to use Numpy to transpose a matrix in Python:

	>>> import numpy as np
	>>> arr = np.array([[1,2,3], [4,5,6]])
	>>> arr_transpose = arr.transpose()
	>>> print(arr_transpose)

Output:
	[[1 4]
	 [2 5]
	 [3 6]]


Using List Comprehension to Transpose Matrix in Python
------------------------------------------------------
Python also provides an alternative method to transpose a matrix using list comprehension. The following is an example of how to use it:

	>>> matrix = [[1,2,3], [4,5,6]]
	>>> transpose = [[row[i] for row in matrix] for i in range(len(matrix[0]))]
	>>> print(transpose)

Output:
	[[1, 4], [2, 5], [3, 6]]


Using zip() Function to Transpose Matrix in Python
--------------------------------------------------
The zip() function is another way to transpose a matrix in Python. Here's how to use it:

	>>> matrix = [[1,2,3], [4,5,6]]
	>>> transpose = list(map(list, zip(*matrix)))
	>>> print(transpose)

Output:
	[[1, 4], [2, 5], [3, 6]]


Conclusion
-----------
Transpose is a simple but useful operation in linear algebra. In Python, we can use Numpy, list comprehension or the zip() function to transpose a matrix. Each method has its own advantages and disadvantages, depending on the context in which it is used.
