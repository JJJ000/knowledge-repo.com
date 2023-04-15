---
title: How can an array of zeros be created in Python (or an array of a specific size)?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: To declare an array of zeros in Python, use the following command `array\_name = [0] * size\_of\_array` (replace `array\_name` and `size\_of\_array` with your desired variable names and values).
---

**Contents**

[TOC]

Declaring an array of Zeros in Python

There are different ways to declare an array of zeros in Python:

Method 1: Using the zeros() function of NumPy

NumPy provides a zeros() function that creates an array of given shape and type, filled with zeros. The syntax is as follows:

```python
import numpy as np

array_of_zeros = np.zeros(shape=(3,4), dtype=int)
```

In this example, we imported the NumPy library and used the zeros() function to create an array of zeros with 3 rows and 4 columns, and integer datatype. You can change the shape and datatype as per your requirement.

Method 2: Using the [0] * n method

Another way to create an array of zeros is by using the [0] * n method, where n is the size of the array. Here's how you can use it:

```python
array_of_zeros = [0] * 5
```

In this example, we created an array of 5 zeros by using the [0] * 5 method.

Method 3: Using the numpy.empty() function

You can also use the numpy.empty() function to allocate an array of a certain size, but without initializing its values. Here's an example:

```python
import numpy as np

array_of_zeros = np.empty((2,3))
```

In this example, we used the numpy.empty() function to create an array of size 2x3, without initializing the values. This function provides faster performance compared to numpy.zeros() as it does not initialize the values.

Conclusion

Any of the three methods above will help you declare an array of zeros depending on your preference. For the NumPy method, you need to import the library, while the other two are native to Python.
