---
title: Is it possible for a Python code line to determine its level of indentation nesting?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Yes, it can determine its indentation nesting level by counting the number of leading whitespace characters.
---

**Contents**

[TOC]

Yes, a line of Python code can know its indentation nesting level using the inspect module. Below are the four sections explaining how it can be done:

## Using getouterframes() method
The getouterframes() method of the inspect module can be used to get the call frame stack of the current thread. This can help us to determine the indentation nesting level of the line of code. We can then use the f_locals method to access the local namespace of the frame and get information about the current indentation level.

Here is an example:

```python
import inspect

def get_indentation_level():
    frame = inspect.currentframe().f_back
    return len(inspect.getouterframes(frame)[1][4])

print(get_indentation_level())
```

## Using getsource() method
The getsource() method of the inspect module can be used to get the source code for a given object. We can use this method to get the source code for the current function or code block, and then count the number of whitespace characters at the beginning of the line to determine the indentation level.

Here is an example:

```python
import inspect

def get_indentation_level():
    source = inspect.getsource(get_indentation_level)
    indentation = len(source) - len(source.lstrip())
    return indentation

print(get_indentation_level())
```

## Using linecache.getline() method
The linecache module provides a cache for accessing lines of code from Python source files. We can use the getline() method to get the line of code for the current line number, and then count the number of whitespace characters at the beginning of the line to determine the indentation level.

Here is an example:

```python
import linecache

def get_indentation_level():
    line = linecache.getline(__file__, inspect.currentframe().f_lineno)
    indentation = len(line) - len(line.lstrip())
    return indentation

print(get_indentation_level())
```

## Using a regular expression
We can use a regular expression to match the leading whitespace characters on the current line of code, and then count the number of matches to determine the indentation level.

Here is an example:

```python
import inspect
import re

def get_indentation_level():
    current_line = inspect.currentframe().f_lineno
    source_lines = inspect.getsourcelines(get_indentation_level)[0]
    leading_whitespace = re.match(r'^\s*', source_lines[current_line - 1]).group(0)
    return len(leading_whitespace)

print(get_indentation_level())
```
