---
title: Find the name of the Python script currently running
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: The name of the current script can be retrieved using the \_\_file\_\_ variable.
---

**Contents**

[TOC]

# Method 1

Using `sys.argv`
--------------------------------
The `sys` module provides access to some variables used or maintained by the interpreter and to functions that interact strongly with the interpreter. One such variable is `sys.argv`, which contains the command-line arguments passed to the script.

```python
import sys

print(sys.argv[0])
```

# Method 2

Using `__file__`
--------------------------------
The `__file__` attribute of the `sys` module contains the pathname of the script.

```python
import os

print(os.path.basename(__file__))
```
