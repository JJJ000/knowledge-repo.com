---
title: What is the method to switch a value on and off?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: To toggle a value in Python, use the not operator.
---

**Contents**

[TOC]

## Introduction
In Python, a value can be toggled by changing its state from one to another. This means that if it is `True`, it can be changed to `False` and vice versa. In this tutorial, we will look at how to toggle a value in Python.

## Method 1: Using the not operator
One way to toggle a value in Python is by using the `not` operator. The `not` operator returns the opposite of a boolean value. If the value is `True`, the `not` operator returns `False`, and if the value is `False`, the `not` operator returns `True`. 

```python
x = True
x = not x
print(x) # Output: False
```

In this example, we assign the boolean value `True` to the variable `x`. We then use the `not` operator to toggle the value of `x`. Finally, we print the value of `x`, which is `False`.

## Method 2: Using boolean XOR operator
Another way to toggle a value in Python is by using the boolean XOR (`^`) operator. XOR returns `True` only if one of the operands is true, but not both. So, if the operands are the same, the output will be `False`.

```python
x = True
x = x ^ True
print(x) # Output: False

x = x ^ True
print(x) # Output: True
```

In this example, we assign the boolean value `True` to the variable `x`. We then use the XOR operator to toggle the value of `x`. Finally, we print the value of `x`, which is `False`. We then use the XOR operator again to toggle the value of `x` and print it again, which is `True`.

## Method 3: Using boolean conditional operator
A third way to toggle a value in Python is by using the conditional operator. The conditional operator evaluates the first expression and returns the second expression if the first expression is `False`. If the first expression is `True`, it returns the third expression.

```python
x = True
x = (x == False)
print(x) # Output: False

x = (x == False)
print(x) # Output: True
```

In this example, we assign the boolean value `True` to the variable `x`. We then use the conditional operator to evaluate the expression `(x == False)`. Since the value of `x` is `True`, the expression evaluates to `False`. We then assign the value of the expression to `x`. Finally, we print the value of `x`, which is `False`. We then use the conditional operator again to evaluate the expression `(x == False)` and print it again, which is `True`.

## Conclusion
In conclusion, we have looked at three ways to toggle a value in Python. We can use the `not` operator, XOR operator, or the conditional operator to toggle the value of a boolean variable.
