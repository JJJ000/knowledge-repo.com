---
title: Retrieve the index for the true value in numpy
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the numpy.where() function to get the indices where a boolean condition is true.
---

**Contents**

[TOC]

## Section 1: Introduction
NumPy is a Python library for scientific computing, which provides a powerful array-processing package. This package provides various tools for operating on arrays, including tools for examining and manipulating array objects. In this article, we will discuss how to get the index where the value is true in NumPy.

## Section 2: NumPy where() function
The NumPy where() function is used to return elements from the array if the condition is true. The basic syntax of this function is:

```python
numpy.where(condition, x, y)
```

Here, the condition is a boolean array, x and y are the values or arrays to be returned based on the condition.

## Section 3: Example Usage
We can use the NumPy where() function to get the index where the value is true in NumPy. Here is an example:

```python
import numpy as np
x = np.array([1, 2, 3, 4, 5])
y = x > 3
print(np.where(y))
```

Output:

```
(array([3, 4]),)
```

In the above example, we first created an array 'x' with values from 1 to 5. Then, we created another array 'y' by comparing the elements in x with 3. This returns a boolean array where the value is true for elements greater than 3. Finally, we used the NumPy where() function to get the index where the value is true.

## Section 4: Conclusion
In this article, we discussed how to get the index where the value is true in NumPy. The NumPy where() function is a very useful tool for conditionally selecting values or arrays, which can be used in various array manipulation and computation tasks.
