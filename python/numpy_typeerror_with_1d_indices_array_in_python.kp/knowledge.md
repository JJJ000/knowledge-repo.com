---
title: The error message states that only one-dimensional arrays containing integer values can be used as scalar indices in numpy
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: This error occurs when attempting to index a numpy array with a non-integer or multi-dimensional index array.
---

**Contents**

[TOC]

Introduction
---
This error message is typically encountered when attempting to use a NumPy array as an index for another NumPy array, but the index array has a non-integer data type, or the index array is a non-scalar array (i.e. it has more than one dimension). 

Solution
---
There are a few potential solutions to this error message: 

1. Convert the data type of the index array to an integer data type with the `astype()` method.

```python
import numpy as np

index_array = np.array([1.5, 2.3, 0.7])
data_array = np.array([10, 20, 30])

# Convert index array to integer data type
index_array = index_array.astype(int)

# Use index array to select elements from data array
result = data_array[index_array]

print(result)
# Output: [20 30 10]
```

2. Ensure that the index array is a one-dimensional array with the `ravel()` method.

```python
import numpy as np

index_array = np.array([[0, 2], [1, 2]])
data_array = np.array([10, 20, 30])

# Flatten index array to one dimension
index_array = index_array.ravel()

# Use index array to select elements from data array
result = data_array[index_array]

print(result)
# Output: [10 30 20 30]
```

3. Use boolean masking instead of integer indexing if possible.

```python
import numpy as np

bool_array = np.array([False, True, True])
data_array = np.array([10, 20, 30])

# Use boolean array to select elements from data array
result = data_array[bool_array]

print(result)
# Output: [20 30]
```

Conclusion
---
The `only integer scalar arrays can be converted to a scalar index with 1D numpy indices array` error message can be resolved by converting the data type of the index array to an integer data type, flattening the index array to one dimension, or using boolean masking instead of integer indexing.
