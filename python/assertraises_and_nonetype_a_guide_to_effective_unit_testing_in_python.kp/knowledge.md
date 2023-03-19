---
title: One possible rephrase could be 'tips for correctly utilizing the assertraises() method in unit-testing when dealing with nonetype objects'
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: When testing for exceptions with assertRaises(), pass in the expected exception class as the first argument and the function or code block that raises the exception as the second argument.
---

**Contents**

[TOC]

Section 1: Introduction
---
Unit testing is used to test the functionality of individual units or components of a software application. It is an important step towards ensuring that the code is robust and reliable. The `assertRaises()` method in Python is used to test whether a specific exception is raised when a particular code block is executed. In this guide, we will discuss how to use this method with NoneType objects.

Section 2: Understanding NoneType objects
---
In Python, `None` is a special keyword that represents the absence of a value. A Variable with a None value is of type `NoneType`. `None` is not the same as an empty string, zero or False. It simply signifies the absence of a value. It is often used to initialize variables, return values from functions or indicate an error.

Section 3: Testing NoneType objects with assertRaises()
---
To test whether a function raises a specific exception when passed `None` as an argument, we can use `assertRaises()` method. Below is an example of how to use `assertRaises()` to test for a `TypeError` when passing a `NoneType` object to a function:

```python
import unittest

def divide_num(num1, num2):
    return num1 / num2

class Test(unittest.TestCase):
    def test_divide_by_zero(self):
        with self.assertRaises(TypeError):
            divide_num(None, 3)
```

In this example, we use the `with` statement and `assertRaises()` method to check whether the function `divide_num()` raises a `TypeError` when passed `None` as the first argument. The `assertRaises()` method will catch the exception and verify that it matches the `TypeError` that we expect.

Section 4: Conclusion
---
In conclusion, testing `NoneType` objects with `assertRaises()` method is a straightforward process in Python. We can use the method to test whether a function raises a specific exception when given `None` as an argument. By doing this, we can ensure that our code is robust and handles edge cases correctly.
