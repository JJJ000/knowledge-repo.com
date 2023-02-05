---
title: What is the procedure for deleting certain items from a numpy array?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the numpy.delete() method to remove specific elements from a numpy array.
---

**Contents**

[TOC]

# Section 1: Identifying the Element to Remove

The first step in removing a specific element from a numpy array is to identify the element that needs to be removed. This can be done by using the numpy.where() function to find the index of the element. This function takes an array and a condition as arguments and returns the indices of the elements that satisfy the condition. For example, if we want to find the index of the element with the value 5, we can use the following code:

index = np.where(arr == 5)

# Section 2: Removing the Element

Once the index of the element to be removed has been identified, the element can be removed from the array using the numpy.delete() function. This function takes an array and an index as arguments and returns a new array with the element at that index removed. For example, if we want to remove the element at index 0 from the array, we can use the following code:

new_arr = np.delete(arr, 0)

# Section 3: Alternative Method

An alternative method for removing a specific element from a numpy array is to use the numpy.delete() function with the condition argument. This function takes an array, a condition, and an axis as arguments and returns a new array with the elements that satisfy the condition removed. For example, if we want to remove all elements with the value 5 from the array, we can use the following code:

new_arr = np.delete(arr, np.where(arr == 5), axis=0)

# Section 4: Conclusion

In conclusion, there are two ways to remove a specific element from a numpy array: by identifying the index of the element to be removed and using the numpy.delete() function, or by using the numpy.delete() function with the condition argument.
