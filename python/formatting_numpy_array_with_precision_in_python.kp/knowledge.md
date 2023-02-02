---
title: Display a numpy array in a readable format with a specified level of precision
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Use numpy.set\_printoptions() with the parameters `precision` and `suppress` set to the desired values.
---

**Contents**

[TOC]

### Using numpy.set_printoptions

NumPy provides the `numpy.set_printoptions` function which allows us to set the precision and suppress scientific notation when printing NumPy arrays.

```python
import numpy as np

# Create a sample NumPy array
arr = np.array([1.12345678, 2.34567891, 3.56789012])

# Set the precision and suppress scientific notation
np.set_printoptions(precision=2, suppress=True)

# Print the array
print(arr)
# Output: [1.12 2.35 3.57]
```

### Using numpy.around

We can also use the `numpy.around` function to round the array to the desired precision and then print it.

```python
import numpy as np

# Create a sample NumPy array
arr = np.array([1.12345678, 2.34567891, 3.56789012])

# Round the array to the desired precision
arr_rounded = np.around(arr, decimals=2)

# Print the array
print(arr_rounded)
# Output: [1.12 2.35 3.57]
```
