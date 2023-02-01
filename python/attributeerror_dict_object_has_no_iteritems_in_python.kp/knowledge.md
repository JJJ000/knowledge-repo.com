---
title: The 'dict' object does not have a 'iteritems' attribute
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: This error occurs when attempting to use the iteritems() method on a dictionary object, which is no longer supported in Python 3.
---

**Contents**

[TOC]

# Overview

The 'dict' object has no attribute 'iteritems' error occurs in Python when a user attempts to call the 'iteritems' function on a dictionary object. This error occurs because the 'iteritems' function is not a valid attribute of the dictionary object in Python.

# Cause of Error

The 'dict' object has no attribute 'iteritems' error occurs because the 'iteritems' function is not a valid attribute of the dictionary object in Python. The 'iteritems' function is only available in Python 2.x and is not available in Python 3.x.

# Solution

To resolve this error, the user should use the 'items' function instead of the 'iteritems' function when working with dictionaries in Python. The 'items' function is available in both Python 2.x and Python 3.x and can be used to iterate over the items in a dictionary.
