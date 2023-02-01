---
title: Displaying the Python version in the output
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Print the value of the sys.version variable to output the current Python version.
---

**Contents**

[TOC]

# Section 1: Retrieve Python Version

The version of Python can be retrieved using the `sys` module.

```python
import sys
print(sys.version)
```

# Section 2: Output Version

The output of the code above will be the version of Python installed on the system. For example, if Python 3.7.3 is installed, the output will be:

```
3.7.3 (default, Apr 24 2019, 15:29:51) [MSC v.1915 64 bit (AMD64)]
```

# Section 3: Format Output

The output can be formatted to display only the major and minor version numbers, such as `3.7` in the example above. This can be done by using the `split()` method to split the output string at the space character. The first element of the resulting list will contain the version number.

```python
version = sys.version.split(' ')[0]
print(version)
```

# Section 4: Print Version

Finally, the version can be printed to the console using the `print()` function.

```python
print('Python version: ' + version)
```

The output of the code above will be:

```
Python version: 3.7.3
```
