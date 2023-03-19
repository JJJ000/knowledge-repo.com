---
title: Instead of a 1-dimensional array, a column vector y was provided
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: The input should be reshaped using y.reshape(-1,).
---

**Contents**

[TOC]

Introduction
------------
When using Python, it is common to encounter a `ValueError` with the message "a column-vector y was passed when a 1d array was expected". This error can occur when working with certain functions or libraries, and can be frustrating for new users. In this article, we will explore why this error occurs, how to identify it, and what steps can be taken to resolve it.


What is a column-vector?
-------------------------
A column-vector is a mathematical object that consists of a single column of numbers. It is commonly used in linear algebra and is often represented using a matrix. In Python, a column-vector can be created using the `numpy` library by passing a list of numbers to the `numpy.array()` function and then transposing it using the `.T` method. For example:

```
import numpy as np

y = np.array([1, 2, 3]).T
```

This will create a column-vector `y` with the values `[1, 2, 3]`.


Why does the error occur?
-------------------------
The "a column-vector y was passed when a 1d array was expected" error occurs when a function or library expects a 1-dimensional (1d) array, but is instead given a column-vector. This is because a column-vector is technically a 2-dimensional (2d) array with only 1 column, whereas a 1d array has only 1 dimension. Many functions and libraries in Python expect 1d arrays as inputs, and can produce errors if given 2d arrays.


How to resolve the error
------------------------
To resolve the "a column-vector y was passed when a 1d array was expected" error, there are a few steps that can be taken:

1. Check the function or library documentation to see if it explicitly requires a 1d array. If this is the case, you will need to convert your column-vector to a 1d array.

2. Use the `.ravel()` method to convert the column-vector to a 1d array. This method "flattens" the array by concatenating each row into a single row. For example:

   ```
   import numpy as np
   
   y = np.array([1, 2, 3]).T
   y_1d = y.ravel()
   ```

   This will create a 1d array `y_1d` with the values `[1, 2, 3]`.

3. Use the `.reshape()` method to convert the column-vector to a 1d array. This method reshapes the array into a different size or shape. For a column-vector, we can reshape it into a row-vector with a single row using `.reshape((1, -1))`. For example:

   ```
   import numpy as np
   
   y = np.array([1, 2, 3]).T
   y_1d = y.reshape((1, -1))
   ```

   This will create a 1d array `y_1d` with the values `[[1, 2, 3]]`.

By following these steps, you should be able to resolve the "a column-vector y was passed when a 1d array was expected" error and continue using the function or library as intended.
