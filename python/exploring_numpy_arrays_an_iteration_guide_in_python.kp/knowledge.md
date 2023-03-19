---
title: Performing iterations on a numpy array
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: To iterate over a numpy array in Python, use a for loop or a numpy method such as nditer().
---

**Contents**

[TOC]

Overview:

Numpy arrays are efficiently designed data structures for mathematical operations in Python. Iterating over a numpy array means going through its elements one by one, and performing some operation on each element. 

The following sections describe various ways to iterate over a numpy array in Python.

Section 1: Using a for loop 

One of the easiest ways to iterate over a numpy array is using a for loop. For example, consider the following code that creates a numpy array and iterates over it using a for loop:

```
import numpy as np

arr = np.array([1, 2, 3, 4, 5])

for i in arr:
    print(i)
```

This code creates a numpy array and prints its elements one by one. The output will be:

```
1
2
3
4
5
```

Section 2: Using nditer() function 

Numpy provides the `nditer()` function to iterate over a numpy array. This function is useful when we need to access each element of a multi-dimensional numpy array. For example, consider the following code:

```
import numpy as np

arr = np.array([[1, 2], [3, 4]])

for x in np.nditer(arr):
    print(x)
```

This code creates a two-dimensional numpy array and iterates over it using the `nditer()` function. The output will be:

```
1
2
3
4
```

Section 3: Using ndenumerate() function 

If we want to iterate over a numpy array and also get the index of each element, we can use the `ndenumerate()` function. For example, consider the following code:

```
import numpy as np

arr = np.array([1, 2, 3, 4, 5])

for idx, val in np.ndenumerate(arr):
    print(idx, val)
```

This code creates a numpy array and iterates over it using the `ndenumerate()` function, which returns the index and value of each element. The output will be:

```
(0,) 1
(1,) 2
(2,) 3
(3,) 4
(4,) 5
```

Section 4: Using vectorized functions 

Numpy provides vectorized functions that can perform operations on entire arrays at once, without iterating over each element. These functions are generally faster and more efficient than iterating over a numpy array. For example, consider the following code that uses a vectorized function to determine if each element of a numpy array is greater than 3:

```
import numpy as np

arr = np.array([1, 2, 3, 4, 5])

mask = arr > 3

print(mask)
```

This code creates a numpy array and applies the vectorized function `>` to each element of the array. The output will be:

```
[False False False  True  True]
```

Here, `mask` is a boolean numpy array that indicates which elements of `arr` are greater than 3. 

Conclusion:

In this article, we discussed four different ways to iterate over a numpy array in Python. With the use of the for loop, `nditer()` function, `ndenumerate()` function and vectorized functions, we can iterate over a numpy array efficiently in Python.
