---
title: What is the purpose of the __future__ module in python, when should it be used, and how does it work?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: \_\_future\_\_ is used for enabling future language features in Python, and is typically used at the beginning of a module to ensure that features from a newer version of Python are available in an older version.
---

**Contents**

[TOC]

## What is __future__?

The __future__ module in Python is used to provide features which are not available in the current version of Python. It allows you to use features from future versions of Python in your current version.

## How Does it Work?

The __future__ module works by providing access to the new features of Python before they are released. When you import the __future__ module, it will automatically enable the new features. This allows you to use them in your code, even if they are not present in the current version of Python.

## When to Use it?

The __future__ module should be used when you want to use features from future versions of Python in your current version. This allows you to use the new features without having to upgrade your Python version.

## How to Use it?

To use the __future__ module, you must first import it in your code. This is done by using the import statement:

```
import __future__
```

Once the module is imported, you can access the new features by using the feature name. For example, if you wanted to use the new print function in Python 3.x, you could do so by using the following code:

```
from __future__ import print_function

print("Hello World!")
```
