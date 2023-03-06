---
title: What is the method for identifying/altering the current directory within the Python shell?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: To know the current directory use the command os.getcwd() and to change the current directory use the command os.chdir(`path/to/directory`).
---

**Contents**

[TOC]

Section 1: What is a current directory?

A current directory is the directory that the user is currently working in or the default directory where files are being stored or fetched from. It is usually set by the operating system when the user logs in or when a new session is started. 

Section 2: How to know the current directory in Python shell?

Python has a built-in module called "os" that provides functions for interacting with the operating system. To get the current directory in Python shell, we can use the getcwd() method from the os module.

```python
import os
print(os.getcwd())
```

This will print the absolute path of the current directory. 

Section 3: How to change the current directory in Python shell?

To change the current directory in Python shell, we can use the chdir() method from the os module. We need to provide the new directory path as a parameter to the chdir() method.

```python
import os
os.chdir('/path/to/new/directory')
```

This will change the current directory to the directory specified in the parameter. 

Section 4: Conclusion

In conclusion, Python provides a simple way to get and change the current directory in the Python shell using the os module. We can use the getcwd() method to get the current directory and the chdir() method to change the current directory.
