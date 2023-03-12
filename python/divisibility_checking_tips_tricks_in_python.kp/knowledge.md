---
title: What is the process for determining if one number is divisible by another number?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the modulo operator (%) to check if there is a remainder when dividing the two numbers. If the remainder is zero, then the first number is divisible by the second number.
---

**Contents**

[TOC]

Checking if a Number is Divisible by Another Number in Python

To check if a number is divisible by another number in Python, you need to use the modulo operator (%). The modulo operator returns the remainder after division, so if the remainder is 0, then the first number is divisible by the second number. Here's how you can check if a number is divisible by another number in Python:

### Using the Modulo Operator

```python
num1 = 10
num2 = 5

if num1 % num2 == 0:
    print(num1, "is divisible by", num2)
else:
    print(num1, "is not divisible by", num2)
```

In this example, we have two numbers `num1` and `num2`. We use the modulo operator to check if `num1` is divisible by `num2`. If the remainder is 0, we print a message indicating that `num1` is divisible by `num2`, otherwise, we print a message indicating that `num1` is not divisible by `num2`.

### Using a Function

```python
def is_divisible(num1, num2):
    if num1 % num2 == 0:
        return True
    else:
        return False

print(is_divisible(10, 5))
```

In this example, we define a function `is_divisible` that takes two parameters `num1` and `num2`. Inside the function, we use the modulo operator to check if `num1` is divisible by `num2`. If the remainder is 0, we return True, otherwise, we return False. 

Finally, we call the function with the arguments `10` and `5` and print the result to the console.

### Using the Divmod Function

```python
num1 = 10
num2 = 5

if divmod(num1, num2)[1] == 0:
    print(num1, "is divisible by", num2)
else:
    print(num1, "is not divisible by", num2)
```

The divmod() function takes two arguments and returns a tuple of two values: the quotient and the remainder. In this example, we are interested only in the remainder. Therefore, we take the second value (indexing starts from 0) of the returned tuple and check if it is 0. If the remainder is 0, the first number is divisible by the second number.
