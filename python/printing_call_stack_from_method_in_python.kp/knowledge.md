---
title: Display the sequence of method calls leading up to the current method in the program's code
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Printing the current call stack from a method in Python can be done using the traceback module`s print\_stack() function.
---

**Contents**

[TOC]

#### Section 1: Importing the Necessary Modules

```python
import inspect 
```

#### Section 2: Getting the Current Call Stack

```python
stack = inspect.stack()
```

#### Section 3: Iterating Through the Stack

```python
for frame in stack:
    print(frame)
```

#### Section 4: Printing the Current Call Stack

```python
print(inspect.stack()[0][3])
```
