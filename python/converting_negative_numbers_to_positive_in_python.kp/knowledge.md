---
title: What is the process for changing a negative number into a positive one?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Use the abs() function in Python to convert a negative number to positive.
---

**Contents**

[TOC]

## Introducing the Problem

Sometimes, when working with numbers in Python, we may need to convert a negative number to its positive counterpart. There are several ways to do this in Python, and in this tutorial, we will cover some of the most common methods.

## Using the abs() Function

One of the easiest and most straightforward ways to convert a negative number to positive in Python is by using the built-in `abs()` function. This function takes a single argument, which can be any numeric value, and returns its absolute value, which is always positive.

```python
num = -10
abs_num = abs(num)
print(abs_num)
```

Output:
```
10
```

## Using the math.fabs() Function

Another option is to use the `fabs()` function from the `math` module, which also returns the absolute value of a number. However, unlike `abs()`, `math.fabs()` can handle floating-point values as well as integers.

```python
import math

num = -10.5
abs_num = math.fabs(num)
print(abs_num)
```

Output:
```
10.5
```

## Multiplying by -1

A third method of converting negative numbers to positive is to multiply the number by -1. This method effectively changes the sign of the number, making it positive if it was negative originally. 

```python
num = -10
pos_num = num * -1
print(pos_num)
```

Output:
```
10
```

## Using the conditional operator

We can also create a conditional statement to check if the given number is negative or not, and then perform appropriate actions accordingly. Here, we can implement the **ternary operator** to reduce code and make it look more elegant.

```python
num = -10
pos_num = num if num >= 0 else -num
print(pos_num)
```

Output:
```
10
```

## Conclusion

These are some of the most common methods for converting negative numbers to positive in Python. Depending on your use case, one method may be more suitable than the others. By using these methods, you can easily manipulate negative numbers in your Python programs.
