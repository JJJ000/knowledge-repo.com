---
title: What is the method to retrieve the separator used in the path environment variable in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: The PATH environment-variable separator in Python can be retrieved using os.pathsep.
---

**Contents**

[TOC]

Getting the PATH Environment-Variable Separator in Python

Section 1: Introduction
Python provides an easy way to get the PATH environment-variable separator using the `os` module. The PATH environment-variable separator is used to separate different directories in the PATH environment variable.

Section 2: Using the `os` Module
To get the PATH environment-variable separator using the `os` module, we can use the `os.pathsep` attribute. The `os.pathsep` attribute returns a string that represents the PATH environment-variable separator.

```python
import os
separator = os.pathsep
print(separator)
```

Output:

```
;  # On Windows
:  # On Unix and macOS
```

Section 3: Conditional Checking
Since the PATH environment-variable separator is different for different operating systems, it is better to check the current operating system before using the `os.pathsep` attribute. We can use the `os.name` attribute to retrieve the name of the current operating system.

```python
import os
if os.name == 'posix':
    # Unix-based, including macOS
    separator = ':'
else:
    # Windows-based
    separator = ';'
print(separator)
```

Output:

```
;  # On Windows
:  # On Unix and macOS
```

Section 4: Conclusion
Getting the PATH environment-variable separator in Python is simple and easy with the `os` module. By using the `os.pathsep` attribute or conditional checking based on the `os.name` attribute, we can retrieve the PATH environment-variable separator for the current operating system.
