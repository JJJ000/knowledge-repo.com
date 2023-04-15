---
title: The difference between 'assertequals' and 'assertequal' in Python can be explained as follows
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: There is no difference between assertEquals and assertEqual in python, they are aliases of each other and can be used interchangeably.
---

**Contents**

[TOC]

Introduction
--------------
Python has a built-in module called `unittest` which provides a framework for unit testing. This module includes various assertion methods like `assertEquals()` and `assertEqual()`, which can be used to check whether the expected result matches the actual result or not. 

Syntax
----------
Both `assertEquals()` and `assertEqual()` methods have similar syntax. The syntax of `assertEquals()` is:

```python
unittest.TestCase.assertEquals(first, second, msg=None)
```
where `first` is the expected value, `second` is the actual value, and `msg` is the message to be displayed when the assertion fails.

The syntax of `assertEqual()` is:

```python
unittest.TestCase.assertEqual(first, second, msg=None)
```
where `first`, `second`, and `msg` are the same as in `assertEquals()`.

Difference between assertEquals and assertEqual
----------------------------------------------------
`assertEquals()` and `assertEqual()` are essentially the same method with different names. In earlier versions of Python, `assertEquals()` was used, while in newer versions, `assertEqual()` is used. There are no functional differences between the two methods. However, the use of `assertEqual()` is preferred since it is more concise and easier to type.

Example
-----------
Let's consider an example to illustrate the use of `assertEquals()` and `assertEqual()` methods:

```python
import unittest

class TestStringMethods(unittest.TestCase):
    
    def test_upper(self):
        self.assertEqual('hello'.upper(), 'HELLO')
        
    def test_is_upper(self):
        self.assertTrue('HELLO'.isupper())
        self.assertFalse('Hello'.isupper())
        
if __name__ == '__main__':
    unittest.main()
```
In this example, we have two test cases that check whether the `upper()` method converts the string to uppercase and whether the `isupper()` method returns `True` for uppercase strings and `False` for lowercase strings. The `assertEqual()` method is used to compare the expected and actual results of `upper()` method, while both `assertEqual()` and `assertTrue()`/`assertFalse()` methods are used to check the output of `isupper()` method.

Conclusion
--------------
In conclusion, `assertEquals()` and `assertEqual()` methods are synonyms in Python and can be used interchangeably. However, `assertEqual()` is the preferred method due to its brevity and readability.
