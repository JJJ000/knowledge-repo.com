---
title: What is the process for choosing elements from an array based on a condition?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Use a list comprehension or filter function with a boolean condition to select elements of an array that meet the specified condition.
---

**Contents**

[TOC]

## Introduction
In Python, arrays can be selected based on certain conditions using boolean indexing. Boolean indexing is a powerful tool that allows you to select elements from an array based on a given condition. In this tutorial, you'll learn how to select elements of an array based on a condition in Python.

## Using Boolean Indexing
Boolean indexing is a technique that allows you to filter an array based on a condition. The condition can be anything: you can filter the array based on values greater than, less than, or equal to a certain value, or based on a combination of conditions. The syntax for boolean indexing is simple: you pass a boolean mask to your array, and it returns an array of only the values that meet that condition.

```python
import numpy as np

array = np.array([1, 2, 3, 4, 5])

bool_mask = [True, False, True, False, True]

new_array = array[bool_mask]

print(new_array)
```

In the above example, we created a boolean mask that is a list of True and False values. This mask is passed to our array using the square bracket notation, and it returns a new array that only contains the values where the mask is True. Here's the output of the above program:

```
[1 3 5]
```

## Using Comparison Operators
You can also filter an array based on values that are greater than, less than, or equal to a certain value. To do this, you use comparison operators like ==, !=, <, >, <=, or >=. Here's an example:

```python
import numpy as np

array = np.array([1, 2, 3, 4, 5])

bool_mask = array > 3

new_array = array[bool_mask]

print(new_array)
```

In the above example, the boolean mask is created by performing a comparison using the "greater than" operator on our array. This returns a boolean mask of True and False values. The values where the mask is True are then used to index the original array, and a new array is created with only the values that meet the condition. Here's the output of the above program:

```
[4 5]
```

## Using Logical Operators
You can also filter an array based on a combination of conditions by using logical operators like "and", "or", and "not". Here's an example:

```python
import numpy as np

array = np.array([1, 2, 3, 4, 5])

bool_mask = (array > 2) & (array < 5)

new_array = array[bool_mask]

print(new_array)
```

In the above example, the boolean mask is created by performing two comparisons using the "greater than" and "less than" operators on our array. These comparisons are then combined using the "&" operator to create a boolean mask of True and False values. The values where the mask is True are then used to index the original array, and a new array is created with only the values that meet the condition. Here's the output of the above program:

```
[3 4]
```

## Conclusion
In conclusion, boolean indexing is a powerful tool that allows you to select elements from an array based on a given condition. By using comparison and logical operators, you can create complex conditions that filter your array to meet specific requirements. With these techniques, you can easily extract the data you need from your arrays and perform your data analysis tasks more efficiently.
