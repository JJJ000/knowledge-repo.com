---
title: Transform a numpy array into a tuple
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To convert a numpy array to tuple in Python, use the tuple() function.
---

**Contents**

[TOC]

### Section 1: Understanding numpy arrays

NumPy is a library in Python that is used for numerical calculations. NumPy arrays are like lists, but they are optimized for mathematical operations. NumPy arrays are faster and require less memory than Python lists. In NumPy, arrays are represented by the `ndarray` class.

### Section 2: Converting a numpy array to a tuple

To convert a NumPy array to a tuple, we can use the `tolist()` method of the NumPy array. The `tolist()` method returns a nested Python list, which can be easily converted to a tuple using the `tuple()` function.

Here's an example code snippet:

```python
import numpy as np

arr = np.array([1, 2, 3, 4, 5])
tup = tuple(arr.tolist())

print(tup)
```

In this code snippet, we first create a NumPy array `arr` with values 1 to 5. Then, we convert the NumPy array to a list using the `tolist()` method. Finally, we convert the list to a tuple using the `tuple()` function and store it in the variable `tup`. The output of this code snippet will be:

```
(1, 2, 3, 4, 5)
```

### Section 3: Converting a multidimensional numpy array to a tuple

If we have a multidimensional NumPy array, we need to first flatten it before we can convert it to a tuple. Flattening means converting a multidimensional array to a one-dimensional array. We can use the `ravel()` method of the NumPy array to flatten it.

Here's an example code snippet:

```python
import numpy as np

arr = np.array([[1, 2], [3, 4], [5, 6]])
flat_arr = arr.ravel()
tup = tuple(flat_arr.tolist())

print(tup)
```

In this code snippet, we first create a two-dimensional NumPy array `arr`. We flatten the array using the `ravel()` method and store it in a variable `flat_arr`. Then, we convert the flattened array to a list using the `tolist()` method and convert the list to a tuple using the `tuple()` function. Finally, we store the tuple in the variable `tup`. The output of this code snippet will be:

```
(1, 2, 3, 4, 5, 6)
```

### Section 4: Conclusion

In this tutorial, we learned how to convert a NumPy array to a tuple in Python. We saw two different examples, one for a one-dimensional array and one for a multidimensional array. We used the `tolist()` method of the NumPy array to convert it to a list, and then used the `tuple()` function to convert the list to a tuple.
