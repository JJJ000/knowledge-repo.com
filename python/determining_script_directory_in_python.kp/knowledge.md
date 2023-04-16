---
title: What is the correct way to identify the directory of the current script?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The current script directory can be determined using the os.path.dirname(os.path.realpath(\_\_file\_\_)) function.
---

**Contents**

[TOC]

**Section 1: Using `__file__`**

The `__file__` variable can be used to get the path of the current script. It can be used in the following way:

```python
import os

script_dir = os.path.dirname(__file__)
```

**Section 2: Using `os.getcwd()`**

The `os.getcwd()` function can be used to get the current working directory. It can be used in the following way:

```python
import os

script_dir = os.getcwd()
```

**Section 3: Using `os.path.abspath()`**

The `os.path.abspath()` function can be used to get the absolute path of the current script. It can be used in the following way:

```python
import os

script_dir = os.path.abspath(__file__)
```

**Section 4: Using `os.path.realpath()`**

The `os.path.realpath()` function can be used to get the canonical path of the current script. It can be used in the following way:

```python
import os

script_dir = os.path.realpath(__file__)
```
