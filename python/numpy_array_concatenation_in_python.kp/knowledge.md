---
title: Combine one numpy array with another numpy array through concatenation
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the NumPy function `numpy.concatenate()` to concatenate two NumPy arrays in Python.
---

**Contents**

[TOC]

Introduction:

In NumPy, concatenation refers to joining two or more arrays together either column-wise or row-wise. The concatenation process is simple and comes with built-in functions. In this tutorial, we will see how to concatenate a NumPy array to another NumPy array in Python using different methods.

Method 1: Using vstack() and hstack() functions:

The vstack() function is used to stack the given arrays vertically, row-wise. It takes a sequence of arrays as input, and returns a single vertical stack of these arrays. The hstack() function is used to stack the given arrays horizontally, column-wise. It takes a sequence of arrays as input, and returns a single horizontal stack of these arrays.

For instance, let us consider two NumPy arrays x and y containing integer values. Our aim is to concatenate y to the bottom of x. The code for this task will be:

```Python
    import numpy as np 
    x = np.array([[1, 2], [3, 4]]) 
    y = np.array([[5, 6]]) 
    print("Original arrays:") 
    print(x) 
    print(y) 
    # Concatenating arrays vertically 
    z = np.vstack((x,y)) 
    print("After concatenating:\n",z)
```

Here, first, we imported the NumPy package and created two arrays x and y. Then, we used the vstack() function to concatenate y to the bottom of x, which resulted in a new array z. Finally, we printed the original and concatenated arrays to check the result.

Method 2: Using concatenate() function:

The concatenate() function of NumPy library is extensively used for concatenation. It is a versatile method for joining two or more arrays along various axes with optional explicit specification of the dimension for concatenation.

The syntax for concatenate() function is as follows:

```Python
    numpy.concatenate((arr1, arr2, ...), axis=0)
```

It accepts two or more arrays along different axes (according to the value specified in the axis parameter) and returns a concatenated array. The default value of the axis parameter is 0.

Consider the same two NumPy arrays x and y as in Method 1. Now, we will use the concatenate() method to concatenate y to the bottom of x. The code for this task will be:

```Python
    import numpy as np 
    x = np.array([[1, 2], [3, 4]]) 
    y = np.array([[5, 6]]) 
    print("Original arrays:") 
    print(x) 
    print(y) 
    # Concatenating arrays horizontally 
    z = np.concatenate((x, y), axis = 0) 
    print("After concatenating:\n",z)
```

Here, we imported the NumPy package and created two arrays x and y. Then, we used the concatenate() method to concatenate y to the bottom of x, which resulted in a new array z. Finally, we printed the original and concatenated arrays to check the result.

Method 3: Using append() function:

The append() method is used to add values or elements to a NumPy array. We can also use this method for concatenation. It accepts an array and axis parameters for concatenation.

The syntax for append() method is as follows:

```Python
    numpy.append(arr, values, axis = None)
```

The axis parameter specifies the axis along which values need to be concatenated. If it is not provided, then the array is flattened.

Consider the same two NumPy arrays x and y as in Method 1. Now, we will use the append() method to concatenate y to the bottom of x. The code for this task will be:

```Python
    import numpy as np 
    x = np.array([[1, 2], [3, 4]]) 
    y = np.array([[5, 6]]) 
    print("Original arrays:") 
    print(x) 
    print(y) 
    # Concatenating arrays horizontally 
    z = np.append(x, y, axis = 0) 
    print("After concatenating:\n",z)
```

Here, we imported the NumPy package and created two arrays x and y. Then, we used the append() method to concatenate y to the bottom of x, which resulted in a new array z. Finally, we printed the original and concatenated arrays to check the result.

Method 4: Using insert() function:

The insert() function is used to insert values along with the given axis before the specified index position. We can use this method for concatenation as well.

The syntax for insert() method is as follows:

```Python
    numpy.insert(arr, obj, values, axis = None)
```

Here, obj is the index position where we want to add new values.

Consider the same two NumPy arrays x and y as in Method 1. Now, we will use the insert() method to concatenate y to the bottom of x. The code for this task will be:

```Python
    import numpy as np 
    x = np.array([[1, 2], [3, 4]]) 
    y = np.array([[5, 6]]) 
    print("Original arrays:") 
    print(x) 
    print(y) 
    # Concatenating arrays horizontally 
    z = np.insert(x, 2, y, axis = 0) 
    print("After concatenating:\n",z)
```

Here, we imported the NumPy package and created two arrays x and y. Then, we used the insert() method to concatenate y to the bottom of x at the index position 2, which resulted in a new array z. Finally, we printed the original and concatenated arrays to check the result.

Conclusion:

In this tutorial, we have discussed different methods to concatenate a NumPy array to another NumPy array in Python. We have explored various functions like vstack(), hstack(), concatenate(), append(), and insert() to achieve this task. We hope this tutorial will help you in your future endeavors.
