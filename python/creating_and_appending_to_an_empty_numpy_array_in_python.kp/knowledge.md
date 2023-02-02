---
title: What is the process for creating an empty array and adding elements to it using numpy?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: To create an empty array and then append to it in NumPy, use the np.append() function.
---

**Contents**

[TOC]

# Creating an Empty Array

To create an empty array in NumPy, one can use the `np.empty()` function. This function takes in the desired shape of the array as an argument and returns an empty array of that shape.

```
import numpy as np

empty_array = np.empty((3,4))
```

# Appending to the Array

To append elements to the empty array, one can use the `np.append()` function. This function takes in the array to which elements are to be appended and the elements to be appended as arguments.

```
import numpy as np

empty_array = np.empty((3,4))

# Append elements to the empty array
np.append(empty_array, [1,2,3,4])
```

# Output

The output of the above code will be an array with the appended elements.

```
array([[ 0.,  0.,  0.,  0.],
       [ 0.,  0.,  0.,  0.],
       [ 0.,  0.,  0.,  0.],
       [ 1.,  2.,  3.,  4.]])
```
