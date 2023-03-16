---
title: What are the correct methods for saving and loading numpy.array() data?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-15 00:00:00
updated_at: 2023-03-15 00:00:00
tldr: To save and load numpy.array() data properly in Python, use the np.save() and np.load() functions respectively.
---

**Contents**

[TOC]

## Introduction

`numpy` is a popular library of Python that is widely used to manipulate arrays or multidimensional arrays. The `numpy` arrays are efficient and fast in performing numeric operations. The arrays can be saved to and loaded from files easily. In this article, we will discuss how to save and load `numpy` arrays in Python.

## Saving Numpy Arrays

There are several ways to save `numpy` arrays to a file. Here are a few popular methods:


### Using `np.save()`

`numpy` provides the `np.save()` function to save a `numpy` array to a file. The function saves the array to a binary file of `.npy` extension. The file name can be specified as an argument of the function. Here is an example:

```
import numpy as np

# Create a numpy array
arr = np.array([1, 2, 3, 4, 5])

# Save the array to a file
np.save('myarray.npy', arr)
```

Here, we created a `numpy` array and saved it in a file named `myarray.npy`. We can load this array later using the `np.load()` function.


### Using `np.savetxt()`

The `np.savetxt()` function is used to save a `numpy` array to a text file. The function takes two arguments: the file name and the array to be saved. Here is an example:

```
import numpy as np

# Create a numpy array
arr = np.array([1, 2, 3, 4, 5])

# Save the array to a text file
np.savetxt('myarray.txt', arr)
```

The `np.savetxt()` function saves the array in a text format with each element separated by a space. The file can be loaded later using the `np.loadtxt()` function.


### Using Python's `pickle` module

`numpy` arrays can also be saved and loaded using Python’s `pickle` module. The `pickle` module is used to convert a Python object into a stream of bytes and vice versa. Here is an example of a `numpy` array being saved and loaded using `pickle`:

```
import numpy as np
import pickle

# Create a numpy array
arr = np.array([1, 2, 3, 4, 5])

# Save the array to a file
with open('myarray.pkl', 'wb') as f:
    pickle.dump(arr, f)

# Load the array from the file
with open('myarray.pkl', 'rb') as f:
    arr = pickle.load(f)
```

Here, we used the `pickle` module to save the `numpy` array to a file named `myarray.pkl`. The `pickle.dump()` method is used to write the object to a file. To load the object from the file, we use the `pickle.load()` method. The `with` statement is used for proper handling of the file stream.


## Loading Numpy Arrays

There are several ways to load `numpy` arrays from files. Here are a few popular methods:

### Using `np.load()`

We can use the `np.load()` function to load a `numpy` array from a `.npy` file. Here is an example:

```
import numpy as np

# Load the array from file
arr = np.load('myarray.npy')

print(arr)
```

The `np.load()` function loads the `numpy` array from the file named `myarray.npy` and returns it. We can then use this array for further processing.


### Using `np.loadtxt()`

We can use the `np.loadtxt()` function to load a `numpy` array from a text file. Here is an example:

```
import numpy as np

# Load the array from file
arr = np.loadtxt('myarray.txt')

print(arr)
```

The `np.loadtxt()` function loads the `numpy` array from the file named `myarray.txt` and returns it. We can then use this array for further processing.


### Using Python's `pickle` module

`numpy` arrays can also be loaded using Python’s `pickle` module. Here is an example of a `numpy` array being loaded using `pickle`:

```
import numpy as np
import pickle

# Load the array from the file
with open('myarray.pkl', 'rb') as f:
    arr = pickle.load(f)

print(arr)
```

Here, we used the `pickle` module to load the `numpy` array from the file named `myarray.pkl`. The `pickle.load()` method is used to read the object from the file. The `with` statement is used for proper handling of the file stream.

## Conclusion

In this article, we discussed how to save and load `numpy` arrays. We learned various methods such as `np.save()`, `np.savetxt()`, and Python's `pickle` module to save `numpy` arrays to files. Similarly, we learned how to use `np.load()`, `np.loadtxt()`, and Python's `pickle` module to load `numpy` arrays from files. These methods can be used to save and load `numpy` arrays for various applications.
