---
title: How can you identify if a numpy array has at least one value that is not numeric?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the numpy function `numpy.isnan()` to check if any element in the array is NaN (Not a Number).
---

**Contents**

[TOC]

## Checking for Null Values

To detect if a NumPy array contains at least one non-numeric value, the first step is to check for null values. This is because null values in NumPy represent non-numeric values. In order to check for null values, we can use the numpy.isnan() method. This method returns an array of the same shape as the input array, with values of True where the input array contains NaN values and False where it does not.

```python
import numpy as np

a = np.array([1, 2, np.nan, 4])

if np.isnan(a).any():
    print('The array contains at least one non-numeric value')
else:
    print('The array contains only numeric values')
```

Output:

```
The array contains at least one non-numeric value
```

This method returns True if there is at least one NaN value in the array, which means that there is at least one non-numeric value in the array.

## Checking for Non-Numeric Values

If the array does not contain any null values, we can check for non-numeric values using the numpy.isfinit() method. This method returns an array of the same shape as the input array, with values of True where the input array contains finite values (i.e., not NaN, not infinity, and not -infinity) and False where it does not.

```python
import numpy as np

a = np.array([1, 2, 3, 4])

if not np.isfinite(a).all():
    print('The array contains at least one non-numeric value')
else:
    print('The array contains only numeric values')
```

Output:

```
The array contains only numeric values
```

This method returns False if there is at least one non-finite value in the array, which means that there is at least one non-numeric value in the array. We use the not operator to check for non-numeric values in this case, since we want to know if there is at least one non-finite value.

## Combining the Two Methods

To cover all cases, we can combine the two methods by first checking for null values and then checking for non-numeric values.

```python
import numpy as np

a = np.array([1, 2, np.nan, 4])

if np.isnan(a).any() or not np.isfinite(a).all():
    print('The array contains at least one non-numeric value')
else:
    print('The array contains only numeric values')
```

Output:

```
The array contains at least one non-numeric value
```

This method returns True if there is at least one NaN value or at least one non-finite value in the array, which means that there is at least one non-numeric value in the array. This covers all possible cases.
