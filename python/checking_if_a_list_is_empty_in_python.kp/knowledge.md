---
title: Is there a way to determine if a list is empty?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can check if a list is empty in Python by using the "if not list" expression.
---

**Contents**

[TOC]

### Using an If Statement

If you want to check if a list is empty using an if statement, you can use the following syntax:

```python
if not list_name:
    # List is empty
```

This will check if the list is empty and if it is, it will execute the code inside the if statement.

### Using the Len Function

You can also use the len function to check if a list is empty. The len function returns the number of items in a list. If the list is empty, the len function will return 0.

```python
if len(list_name) == 0:
    # List is empty
```

### Using the Any Function

The any function checks if any item in a list is true. If all items in the list are false, the any function will return False.

```python
if not any(list_name):
    # List is empty
```

### Using the All Function

The all function checks if all items in a list are true. If any item in the list is false, the all function will return False.

```python
if not all(list_name):
    # List is empty
```
