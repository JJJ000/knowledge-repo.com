---
title: What is the programmatic method for obtaining the location of python.exe?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: You can get the python.exe location programmatically using the `sys.executable` attribute.
---

**Contents**

[TOC]

## Import sys module 

The `sys` module provides access to some variables used or maintained by the interpreter and to functions that interact strongly with the interpreter.

```python
import sys
```

## Access the executable path

The `sys.executable` variable contains the full path of the currently running Python interpreter.

```python
python_location = sys.executable
```

## Print the executable path

You can print the `python_location` variable to display the current location of the `python.exe` file.

```python
print(python_location)
```

## Complete code

Here is the complete code that demonstrates how to get the Python executable location programmatically:

```python
import sys

python_location = sys.executable
print(python_location)
```
