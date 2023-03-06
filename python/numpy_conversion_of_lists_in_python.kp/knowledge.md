---
title: Convert a set of lists into a numpy array
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: To convert a list of lists into a numpy array in Python, use the numpy.array() function.
---

**Contents**

[TOC]

## Importing numpy library

Before we start creating numpy array from list of lists, we need to import the numpy library in our python code. We can do this by using the following code: 

```python
import numpy as np
```

This will enable us to use numpy functions and methods in our code.

## Creating numpy array from list of lists

We can create numpy array from list of lists using the `numpy.array()` method. The syntax for this method is as follows: 

```python
numpy.array(object, dtype=None, copy=True, order='K', subok=False, ndmin=0)
```

We can pass a list of lists as the `object` parameter to create numpy array. The dtype parameter specifies the data type of the elements in the array. If this parameter is not specified, numpy will infer the data type based on the elements in the array.

## Example

Let's take an example to understand how to create numpy array from list of lists. 

```python
import numpy as np

lst = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
arr = np.array(lst)

print(arr)
```

Output:

```
[[1 2 3]
 [4 5 6]
 [7 8 9]]
```

In this example, we have created a list of lists `lst` with 3 inner lists of length 3. We have then passed this list to the `numpy.array()` method to create numpy array `arr`. Finally, we have printed the numpy array.

## Conclusion

In this tutorial, we have learned how to create numpy array from list of lists in python. We have also learned about the syntax of the `numpy.array()` method and its parameters.
