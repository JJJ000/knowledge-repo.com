---
title: Detecting maximum and minimum values within a one-dimensional numpy array using numpy
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the numpy functions `argmax` and `argmin` to find the indices of the local maxima and minima, respectively.
---

**Contents**

[TOC]

# Introduction

Numpy is a powerful Python library for numerical computations. It provides us with several functions that we can use to perform various mathematical operations, including finding local maxima and minima in a 1D numpy array. In this tutorial, we will learn how to find local maxima and minima in 1D numpy arrays using Numpy functions.

# Importing Numpy

The first step is to import the Numpy library. We can use the following command to import Numpy:

``` python
import numpy as np
```
# Finding local maxima and minima

Numpy provides us with two functions to find local maxima and minima in a 1D numpy array: ```argrelextrema()``` and ```argmin()```/```argmax()```.

## Using argrelextrema()

The ```argrelextrema()``` function returns the indices of the local maxima and minima in a 1D numpy array. We can use the following code to find the local maxima and minima:

``` python
import numpy as np
from scipy.signal import argrelextrema

# create a 1D numpy array
a = np.array([3, 2, 4, 1, 5, 2, 6, 7, 2, 4])

# find local maxima and minima
maxima_indices = argrelextrema(a, np.greater)
minima_indices = argrelextrema(a, np.less)

print("Local maxima indices:", maxima_indices)
print("Local minima indices:", minima_indices)
```

The ```argrelextrema()``` function takes two arguments: the array for which we want to find the local maxima/minima and the order of the derivative. In this example, we have used ```np.greater``` and ```np.less``` as the order of the derivative to find the local maxima and minima, respectively.

## Using argmin() and argmax()

Alternatively, we can use the ```argmin()``` and ```argmax()``` functions to find the indices of the minimum and maximum values in a 1D numpy array. Here is how we can find local minima and maxima using these functions:

``` python
import numpy as np

# create a 1D numpy array
a = np.array([3, 2, 4, 1, 5, 2, 6, 7, 2, 4])

# find local minima and maxima
min_index = np.argmin(a)
max_index = np.argmax(a)

print("Local minima index:", min_index)
print("Local maxima index:", max_index)
```

In this example, we simply used the ```argmin()``` and ```argmax()``` functions to find the indices of the minimum and maximum values in the array.

# Conclusion

In this tutorial, we learned how to find local maxima and minima in a 1D numpy array using Numpy functions. We used the ```argrelextrema()``` function to find both local maxima and minima and the ```argmin()``` and ```argmax()``` functions to find local minima and maxima, respectively. These functions are very useful when we want to analyze data and find the peaks and valleys in a dataset.
