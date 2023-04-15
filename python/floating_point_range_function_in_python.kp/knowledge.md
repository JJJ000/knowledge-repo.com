---
title: A function that provides a sequence of floating-point numbers is called as a 'range() for floats'
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: There is no built-in range() function for floats in Python, but it can be implemented using a custom function.
---

**Contents**

[TOC]

Section 1: Understanding the range() function
The range() function in Python is used to generate a sequence of numbers within a specific range. The function takes three arguments: start, stop, and step. The start argument is the starting number of the sequence, stop argument is the ending number of the sequence, and step is the difference between each number in the sequence. 

Section 2: Limitations of range() function with floats
The range() function only works with integers, and not with floating-point numbers. This means that if you try to use a range() function with floats as start, stop, or step arguments, you will get a TypeError.

Section 3: Workarounds for using range() with floats
One workaround for using range() with floats is to convert the start, stop, and step arguments into integers using the int() function. However, this method will not work for all scenarios, especially if you need a precise increment for your float sequence. Another workaround is to use NumPy's arange() function, which allows you to generate a sequence of float numbers. 

Section 4: Using NumPy's arange() function for float sequences
To use NumPy's arange() function for float sequences, you need to import the NumPy library first. Then, you can call the arange() function and pass in the start, stop, and step arguments as floats. The function returns a NumPy array of float numbers within the specified range. For example:

```
import numpy as np

float_range = np.arange(0.1, 1.0, 0.1)
print(float_range)
```

Output:
```
array([0.1, 0.2, 0.3, 0.4, 0.5, 0.6, 0.7, 0.8, 0.9])
```

In this example, we generate a sequence of float numbers between 0.1 and 1.0, with an increment of 0.1. The arange() function returns a NumPy array of float numbers.
