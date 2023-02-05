---
title: Error tkinter module not found
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Tkinter is not a built-in module in Python, so it must be installed separately.
---

**Contents**

[TOC]

# Solution

## Installing Tkinter
The first step in resolving this error is to install the Tkinter module. This can be done using the package manager of your choice, such as `pip` or `conda`. 

For example, in a terminal window, you can use `pip install tkinter` to install the module.

## Importing Tkinter
Once the module is installed, you can import it in your code by using the `import` statement. For example:

```python
import tkinter
```

This will allow you to use the module in your code.

## Troubleshooting
If you are still receiving the error, it is possible that the module is installed in a different location than the one that your code is looking for. To resolve this, you can specify the location of the module when you import it. 

For example:

```python
import tkinter from /path/to/module
```

## Conclusion
In conclusion, the "No module named 'Tkinter'" error can be resolved by installing the Tkinter module and then importing it correctly in your code. If you are still receiving the error, it is possible that the module is installed in a different location than the one that your code is looking for, and you can specify the location of the module when you import it.
