---
title: What is the optimal method for maintaining numpy arrays stored on a disk?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: The best way to preserve numpy arrays on disk in Python is using the numpy.save() and numpy.load() functions.
---

**Contents**

[TOC]

# Introduction
NumPy arrays are widely used in scientific computing and data analysis. It is essential to store and retrieve these arrays efficiently and securely. In this article, we will discuss the best ways to preserve NumPy arrays on disk in Python.

## Using NumPy's save and load functions

NumPy provides the `save()` function to serialize and save a NumPy array to a file. The function takes two arguments – the filename and the array to be saved. We can save the array in several formats, such as .npy, .npz, and .txt. We can load the saved array using the `load()` function.

### Save function

``` python
import numpy as np

# Create a NumPy array
my_array = np.array([[1, 2, 3], [4, 5, 6]])

# Save the NumPy array to a file
np.save('my_array.npy', my_array)
```

### Load function

``` python
import numpy as np

# Load the saved array
my_array = np.load('my_array.npy')

# Print the loaded array
print(my_array)
```

## Using Pickle
We can also use the Python `pickle` module to serialize and store NumPy arrays on disk. The module provides the `dump()` and `load()` functions to write and read the serialized representation of the NumPy array to and from a file.

### Dump function

``` python
import numpy as np
import pickle

# Create a NumPy array
my_array = np.array([[1, 2, 3], [4, 5, 6]])

# Save the NumPy array to a file using pickle
with open('my_array.pkl', 'wb') as f:
    pickle.dump(my_array, f)
```

### Load function

``` python
import numpy as np
import pickle

# Load the saved array using pickle
with open('my_array.pkl', 'rb') as f:
    my_array = pickle.load(f)

# Print the loaded array
print(my_array)
```

## Using HDF5
Another popular format for storing large numerical datasets is HDF5. It is fast, scalable, and widely used in the scientific computing community. We can use the `h5py` library to read and write HDF5 files from Python.

### Installation

``` bash
pip install h5py
```

### Storing array data

``` python
import h5py

# Create a NumPy array
my_array = [[1, 2, 3], [4, 5, 6]]

# Creating file to store the data
f = h5py.File('my_array.h5', 'w')

# Saving array data to the file
f.create_dataset('data', data=my_array)

# Closing the file
f.close()
```

### Retrieving array data

``` python
import h5py

# Opening the file
f = h5py.File('my_array.h5', 'r')

# Retrieving the array data
my_array = f['data'][:]

# Closing the file
f.close()

# Printing the array
print(my_array)
```

## Conclusion
In this article, we discussed three different approaches to store and retrieve NumPy arrays on disk in Python - using NumPy's `save()` and `load()` functions, using Python's `pickle` module, and using HDF5 with `h5py`. The choice of format depends on the size of the array, the required read/write performance, and the specific use case.
