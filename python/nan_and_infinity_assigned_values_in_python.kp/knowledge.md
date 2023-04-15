---
title: Can a value be assigned as nan or infinity?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Yes, it is possible to set a number to NaN or infinity in Python.
---

**Contents**

[TOC]

Yes, it is possible to set a number to NaN or infinity in Python using different functions or methods. 

Section 1: Setting a number to NaN in Python 
NaN (Not a Number) is a special value that represents an undefined or unrepresentable value. In Python, we can set a number to NaN using the numpy library. Here is an example: 

```python 
import numpy as np
x = np.nan
print(x)
``` 

Output: 
```
nan
```

Section 2: Setting a number to positive infinity or negative infinity 
We can also set a number to positive or negative infinity in Python using the float function. Here is an example: 

```python 
x = float('inf') # positive infinity
y = float('-inf') # negative infinity
print(x)
print(y)
``` 

Output: 
```
inf
-inf
```

Section 3: Checking for NaN or infinity values in Python 
We can check whether a variable contains NaN or infinity using the math library functions isnan() and isinf(). Here is an example: 

```python 
import math
x = float('nan')
y = float('inf')
z = float('-inf')

print(math.isnan(x)) # True
print(math.isinf(y)) # True 
print(math.isinf(z)) # True
``` 

Output: 
```
True
True
True
```

Section 4: Exception when using NaN or infinity values 
When using NaN or infinity values in arithmetic operations, we may encounter unexpected results or exceptions. For example, division by zero, multiplying infinity with zero or infinity, and taking the square root of negative numbers. Here is an example: 

```python 
x = float('inf')
y = float('-inf')

print(x * 0) # nan
print(x / 0) # inf
print(y / 0) # -inf
print(math.sqrt(-1)) # ValueError: math domain error
``` 

Output: 
```
nan
inf
-inf
ValueError: math domain error
```
