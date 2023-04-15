---
title: How to set a default value or a specified value in Python argparse?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The default value is used if the argument is not specified, otherwise the specified value is used.
---

**Contents**

[TOC]

Introduction
------------
`argparse` is an important module in Python that allows developers to easily parse command line arguments. One of the important features of `argparse` is the ability to specify default values for arguments. However, sometimes it is necessary to check whether the user has specified a value explicitly or if it is just the default value. In this article, we will explore how to determine whether the value of an argument is the default value or a value explicitly specified by the user.

Using `is None` Test
--------------------
By default, `argparse` sets the value of an argument to `None` if the user doesn't specify a value. We can use this fact to check if the value of an argument is the default value or a user-specified value. Here's how:

```python
import argparse

parser = argparse.ArgumentParser()
parser.add_argument('--option', default='default')

args = parser.parse_args()
if args.option is None :
    print("The default value is being used")
else:
    print("The user has specified a value")
```

Here, we check whether the value of the `option` argument is `None`. If it is, it means that the user didn't specify a value and the default value is being used. Otherwise, the user has specified a value.

Using `default` Parameter
-------------------------
Another way to check if the user has specified a value explicitly or if it is just the default value is to use the `default` parameter of the `add_argument()` method. Here's how:

```python
import argparse

parser = argparse.ArgumentParser()
parser.add_argument('--option', default='default')

args = parser.parse_args()
if args.option == parser.get_default('option'):
    print("The default value is being used")
else:
    print("The user has specified a value")
```

Here, we compare the value of `option` with the default value we specified in the `add_argument()` method using the `get_default()` method of the `ArgumentParser` class. If the value is the same, it means that the default value is being used, otherwise the user has specified a value.

Using `None` and `default` Parameters Together
-----------------------------------------------
If we want to use both of the above methods together, we can do so as well. Here's how:

```python
import argparse

parser = argparse.ArgumentParser()
parser.add_argument('--option', default='default', type=str, nargs='?')

args = parser.parse_args()
if args.option is None:
    print("The default value is being used")
elif args.option == parser.get_default('option'):
    print("The default value is being used")
else:
    print("The user has specified a value")
```

Here, we use the `None` test to determine if the user has specified a value or not. If not, we use the `get_default()` method to check if the default value is being used. If the value is not `None`, we compare with the default value to see if it is the same. If it is, it means the default value is being used, otherwise, the user has specified a value.

Conclusion
----------
In this article, we explored three different methods to determine whether the user has specified a value explicitly or if it is just the default value. Depending on the requirements of your application, you can use any of these methods to check if the user has specified a value or not.
