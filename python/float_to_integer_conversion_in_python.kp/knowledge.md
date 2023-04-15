---
title: What is the nearest integer for a floating-point number when it is rounded down?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the math.floor() function to round down a floating-point number to the nearest integer in Python.
---

**Contents**

[TOC]

Converting float to int 
To round a float down to the nearest integer, we can simply cast it to an integer using the int() function. This will always round down to the nearest whole number, regardless of how close the float is to the next highest whole number. 

```python
x = 3.14
y = int(x)
print(y)
# output: 3
```

Using math.floor()
Another way to round down a float to the nearest integer is to use the math.floor() function. This function returns the largest integer less than or equal to the input number. 

```python
import math

x = 3.14
y = math.floor(x)
print(y)
# output: 3
```

Using integer division
Lastly, we can also round a float down to the nearest integer using integer division. We can do this by dividing the float by 1, which results in an integer value. 

```python
x = 3.14
y = x // 1
print(y)
# output: 3
```

Note that all three methods will give us the same result when rounding a float down to the nearest integer.
