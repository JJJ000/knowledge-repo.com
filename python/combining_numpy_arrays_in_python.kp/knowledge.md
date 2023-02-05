---
title: Combining two single-dimensional numpy arrays
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: You can concatenate two one-dimensional NumPy arrays by using the np.concatenate() function.
---

**Contents**

[TOC]

**Section 1: Creating the Arrays**

First, we need to create the two one-dimensional NumPy arrays that we want to concatenate. We can do this by using the numpy.array() function.

```python
import numpy as np

array_1 = np.array([1,2,3,4,5])
array_2 = np.array([6,7,8,9,10])
```

**Section 2: Concatenating the Arrays**

Now, we can use the numpy.concatenate() function to concatenate the two arrays together.

```python
concatenated_array = np.concatenate((array_1, array_2))
```

**Section 3: Verifying the Concatenation**

We can verify that the arrays were successfully concatenated by printing out the new array.

```python
print(concatenated_array)
```

Output: `[ 1  2  3  4  5  6  7  8  9 10]`

**Section 4: Conclusion**

We have successfully concatenated two one-dimensional NumPy arrays in Python.
