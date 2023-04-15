---
title: How to create custom exceptions in modern python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Create a custom exception class that inherits from the built-in Exception class.
---

**Contents**

[TOC]

# 1. Create a Custom Exception Class 
Creating a custom exception class in Python is very simple. All you need to do is to create a class inheriting from the base Exception class. You can optionally add additional attributes and methods to the class to make it more useful.

# 2. Raising a Custom Exception
Once you have created the custom exception class, you can raise it like any other exception. This can be done using the raise keyword.

# 3. Catching a Custom Exception
You can catch a custom exception in the same way as any other exception. You can use the try-except statement to catch the exception and handle it appropriately.

# 4. Using the with Statement
The with statement can also be used to handle custom exceptions. The with statement ensures that the resources used in the with block are properly released, even if an exception is raised.
