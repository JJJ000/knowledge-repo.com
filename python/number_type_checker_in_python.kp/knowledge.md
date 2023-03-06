---
title: Verify whether a value is of integer or floating point type
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the isinstance() function to check if a number is of the int or float data type in Python.
---

**Contents**

[TOC]

# Checking if a number is an integer in Python

To check if a number is an integer in Python, we can use the `isinstance()` function. 

Here is how we can do it:

```python
x = 5

if isinstance(x, int):
    print("x is an integer")
else:
    print("x is not an integer")
```

Output:
```
x is an integer
```

# Checking if a number is a float in Python

To check if a number is a float in Python, we can again use the `isinstance()` function. 

Here is how we can do it:

```python
x = 5.0

if isinstance(x, float):
    print("x is a float")
else:
    print("x is not a float")
```

Output:
```
x is a float
```

# Checking if a number is either int or float in Python

To check if a number is either an integer or a float in Python, we can use the `isinstance()` function with the `or` operator. 

Here is how we can do it:

```python
x = 5.0

if isinstance(x, int) or isinstance(x, float):
    print("x is either an integer or a float")
else:
    print("x is not an integer or a float")
```

Output:
```
x is either an integer or a float
```

# Checking if a number is not int or float in Python

To check if a number is not an integer or a float in Python, we can use the `not` operator with the `isinstance()` function. 

Here is how we can do it:

```python
x = "5"

if not isinstance(x, int) and not isinstance(x, float):
    print("x is not an integer or a float")
else:
    print("x is either an integer or a float")
```

Output:
```
x is not an integer or a float
```
