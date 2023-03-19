---
title: What is the method to use natural logarithms (e.g. "ln()") with numpy library in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: To do natural logs with numpy in Python, use the function `numpy.log()`.
---

**Contents**

[TOC]

# Importing Numpy

The first step is to import the numpy module so that we can access all its inbuilt functions. This can be done by running the following code: 

``` python
import numpy as np
```

# Using Numpy's `log()` function

Numpy's `log()` function can be used to compute the natural logarithm of a given number or an array. The syntax for using this function is as follows: 

``` python
np.log(x)
```

where `x` can be a number or an array of numbers. 

# Example

Suppose we want to compute the natural logarithm of a number `x = 5`. The following code will achieve that: 

``` python
import numpy as np

x = 5
ln_x = np.log(x)

print(ln_x)
```

The output will be: 

```
1.6094379124341003
```

This means that the natural logarithm of 5 is approximately 1.609.
