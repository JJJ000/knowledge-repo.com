---
title: How to prevent line breaks when using the print statement in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the end parameter in the print() function and set it to an empty string.
---

**Contents**

[TOC]

### Using the end parameter

One way to avoid a newline after a print statement in Python is to use the `end` parameter. By default, the value of `end` is "\n", which adds a new line character at the end of the printed string. However, we can change the value of `end` to something else, such as an empty string. Doing this will prevent a new line character from being added at the end of the printed string.

```python
print("Hello, world!", end='')
```

### Using the escape character

Another way to avoid a new line after a print statement is to use the escape character "\b". This character represents a backspace, and when used at the end of a string, it will remove the last character before the cursor. By using this character, we can remove the new line character that is automatically added at the end of a print statement.

```python
print("Hello, world!\b")
```

### Using the sys module

We can also avoid a new line after a print statement by using the `sys` module. This module provides access to some variables used or maintained by the Python interpreter and to functions that interact strongly with the interpreter. One of the variables provided by this module is `stdout`, which represents the standard output stream. By setting the `end` parameter of `print()` to an empty string and immediately calling `sys.stdout.flush()`, we can print a string without a new line character being added.

```python
import sys
print("Hello, world!", end='')
sys.stdout.flush()
```

### Using the join method

Lastly, we can also use the `join()` method to concatenate strings and avoid a new line character at the end of a print statement. We can create a list with the string we want to print, and then join the list elements together without adding a separator.

```python
print(''.join(["Hello, world!"]))
```
