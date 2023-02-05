---
title: Counting how often each unique value appears in a numpy array
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The NumPy function numpy.unique() can be used to return the unique values and their respective counts in a NumPy array.
---

**Contents**

[TOC]

**Section 1: Creating a NumPy Array**

The first step is to create a NumPy array. We can create a simple array with the following code:

```
import numpy as np

a = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10])
```

**Section 2: Calculating Frequency Counts**

Once the array is created, we can calculate the frequency counts for each unique value. We can do this using the `np.unique()` function, which returns an array of unique values in the given array and their corresponding count.

```
unique_values, counts = np.unique(a, return_counts=True)
```

**Section 3: Printing the Results**

We can print the results of the frequency counts with the following code:

```
for i in range(len(unique_values)):
    print("Value:", unique_values[i], "Count:", counts[i])
```

**Section 4: Output**

The output of the code above will be:

```
Value: 1 Count: 1
Value: 2 Count: 1
Value: 3 Count: 1
Value: 4 Count: 1
Value: 5 Count: 1
Value: 6 Count: 1
Value: 7 Count: 1
Value: 8 Count: 1
Value: 9 Count: 1
Value: 10 Count: 1
```
