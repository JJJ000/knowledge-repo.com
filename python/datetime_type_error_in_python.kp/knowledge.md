---
title: The attribute 'datetime' is not present in the type object 'datetime.datetime'
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: This error occurs when attempting to access the datetime attribute from a datetime.datetime object instead of just using datetime.
---

**Contents**

[TOC]

Section 1: Overview 
If you encounter an error that says "type object 'datetime.datetime' has no attribute 'datetime'" in Python, it means that there is a problem with how you are trying to access the datetime module in Python.

Section 2: Explanation of Error
Datetime is a module in Python used to work with dates and times. When you import the datetime module, you can access the datetime class which allows you to create datetime objects. The error message you are seeing occurs when you try to access the datetime attribute of the datetime module, which doesn't exist.

Section 3: Common Causes of the Error
One common cause of the "type object 'datetime.datetime' has no attribute 'datetime'" error is when you accidentally use datetime as a variable name or use it as the name for a function or class. This can cause Python to interpret the variable or function name as the datetime module, leading to the error message.

Another common cause of the error is when you try to use the datetime attribute as if it were an instance method, rather than the class itself.

Section 4: Solutions for the Error
To fix the "type object 'datetime.datetime' has no attribute 'datetime'" error, ensure that you are using the correct syntax to access the datetime module and its attributes. If you have accidentally named a variable or function datetime, simply rename it to something else. Also, make sure you are using the datetime attribute correctly, as a class rather than an instance method.
