---
title: Numpy array shapes
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: A Numpy array is a multidimensional array of elements, where each element is identified by a tuple of non-negative integers.
---

**Contents**

[TOC]

### 1D Array

A 1D array is an array with only one dimension, containing a single row of data. It can be created like this:

```python
import numpy as np

arr = np.array([1, 2, 3, 4, 5])
```

### 2D Array

A 2D array is an array with two dimensions, containing rows and columns of data. It can be created like this:

```python
import numpy as np

arr = np.array([[1, 2, 3],
                [4, 5, 6],
                [7, 8, 9]])
```

### 3D Array

A 3D array is an array with three dimensions, containing rows, columns, and depth of data. It can be created like this:

```python
import numpy as np

arr = np.array([[[1, 2, 3],
                 [4, 5, 6],
                 [7, 8, 9]],
                [[10, 11, 12],
                 [13, 14, 15],
                 [16, 17, 18]]])
```

### 4D Array

A 4D array is an array with four dimensions, containing rows, columns, depth, and time of data. It can be created like this:

```python
import numpy as np

arr = np.array([[[[1, 2, 3],
                  [4, 5, 6],
                  [7, 8, 9]],
                 [[10, 11, 12],
                  [13, 14, 15],
                  [16, 17, 18]]],
                [[[19, 20, 21],
                  [22, 23, 24],
                  [25, 26, 27]],
                 [[28, 29, 30],
                  [31, 32, 33],
                  [34, 35, 36]]]])
```
