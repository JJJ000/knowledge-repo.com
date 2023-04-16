---
title: Handling an error while executing a Python 'with' block
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can catch an exception using a `try` statement within the `with` block.
---

**Contents**

[TOC]

### Try/Except Block

When using a Python `with` statement, it is possible to catch exceptions using a `try/except` block. For example, the following code will attempt to open a file, and if an exception is raised, it will be caught and handled:

```python
try:
    with open('myfile.txt') as f:
        # do something with the file
except Exception:
    # handle the exception
```

### Context Managers

Another way to catch exceptions while using a Python `with` statement is to use a context manager. A context manager is an object that manages a context of code execution. It can be used to catch exceptions, and also to ensure that resources are correctly released when the code block is finished.

For example, the following code will attempt to open a file, and if an exception is raised, it will be caught and handled by the context manager:

```python
with contextlib.closing(open('myfile.txt')) as f:
    # do something with the file
```

### Finally Block

Finally, it is possible to catch exceptions while using a Python `with` statement by using a `finally` block. The `finally` block will always be executed, regardless of whether an exception was raised or not.

For example, the following code will attempt to open a file, and any exceptions that are raised will be caught and handled in the `finally` block:

```python
try:
    with open('myfile.txt') as f:
        # do something with the file
except Exception:
    # handle the exception
finally:
    # always execute this code
```
