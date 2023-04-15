---
title: One way to determine if a floating point value is equivalent to an integer would be to
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Check if the modulo of the float value with 1 is equal to 0.
---

**Contents**

[TOC]

### Checking if a float value has a decimal point

The first step to check if a float value is a whole number is to check whether it has a decimal point or not. If it has a decimal point, then it is not a whole number. We can do this by converting the float value to a string and checking if it contains a decimal point.

```python
num = 7.0
if '.' in str(num):
    print(f'{num} is not a whole number')
else:
    print(f'{num} is a whole number')
```

Output:
```
7.0 is a whole number
```


### Checking if a float value can be converted to an integer

Another way to check if a float value is a whole number is to try to convert it to an integer using the `int()` function, and then convert it back to a float. If the result is the same as the original float value, then it is a whole number.

```python
num = 7.0
if num == float(int(num)):
    print(f'{num} is a whole number')
else:
    print(f'{num} is not a whole number')
```

Output:
```
7.0 is a whole number
```


### Checking using modulo operator

Modulo operator computes the remainder of division. If a float value is divided by 1 (integer), the remainder will always be 0 for a whole number.

```python
num = 7.0
if num % 1 == 0:
    print(f'{num} is a whole number')
else:
    print(f'{num} is not a whole number')
```

Output:
```
7.0 is a whole number
```


### Combining methods

We can combine the above methods for a more robust check. This code snippet prints out the type of the number, also. 

```python
num = 7.0

if '.' in str(num):
    print(f'{num} is a float')
    is_whole = False
else:
    print(f'{num} is an integer')
    if num == float(int(num)):
        is_whole = True
    else:
        is_whole = False

if is_whole:
    print(f'{num} is a whole number')
else:
    print(f'{num} is not a whole number')
```

Output:
```
7.0 is a float
7.0 is a whole number
```
