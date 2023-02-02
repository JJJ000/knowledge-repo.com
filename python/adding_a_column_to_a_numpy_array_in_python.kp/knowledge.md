---
title: What is the syntax for adding an additional column to a numpy array?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: You can add an extra column to a NumPy array by using the numpy.append() function.
---

**Contents**

[TOC]

**1. Create a new column**

To add a new column to a NumPy array, create a new array with the same shape as the original array and add the new column to it. 

**2. Add the new column to the original array**

Once the new column is created, use the `np.hstack()` function to add the new column to the original array. The syntax for this function is `np.hstack((arr1, arr2))`, where `arr1` is the original array and `arr2` is the new column.

**3. Assign the new array to the original array**

After adding the new column to the original array, assign the new array to the original array. This can be done using the `=` operator. 

**4. Verify the new column**

Finally, use the `np.shape()` function to verify that the new column has been added to the original array. The syntax for this function is `np.shape(arr)`, where `arr` is the array.
