---
title: What are the multiple variables in a 'with' statement?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Multiple variables can be specified in a `with` statement in Python by separating them with commas.
---

**Contents**

[TOC]

#### Variable Declaration
Within a `with` statement, variables can be declared and initialized by using the `as` keyword. For example:

```python
with open('file.txt') as f:
    data = f.read()
```

In the above example, `f` is the variable declared and initialized with the file object returned by the `open()` function. 

#### Multiple Variables
It is also possible to declare multiple variables within a single `with` statement. For example:

```python
with open('file1.txt') as f1, open('file2.txt') as f2:
    data1 = f1.read()
    data2 = f2.read()
```

In the above example, two variables `f1` and `f2` are declared and initialized with the file objects returned by the `open()` function. 

#### Multiple Files
It is also possible to open multiple files within a single `with` statement. For example:

```python
with open('file1.txt', 'r') as f1, open('file2.txt', 'w') as f2:
    data1 = f1.read()
    f2.write(data1)
```

In the above example, two files `file1.txt` and `file2.txt` are opened within the `with` statement. The first file is opened in read mode and the second file is opened in write mode.

#### Context Managers
It is also possible to use multiple context managers within a single `with` statement. For example:

```python
with open('file1.txt') as f1, contextlib.closing(open('file2.txt')) as f2:
    data1 = f1.read()
    data2 = f2.read()
```

In the above example, two context managers are used within the `with` statement. The first context manager is `open()` and the second context manager is `contextlib.closing()`. This allows for more flexibility in managing resources within the `with` statement.
