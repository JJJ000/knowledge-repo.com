---
title: What is the way to obtain the location of the parent directory?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use the os.path.dirname() function with the path of the current directory or file to get the location of its parent directory in Python.
---

**Contents**

[TOC]

Section 1: Introduction
In Python, there are different ways to get the parent directory location. This tutorial will cover four different methods, each with its own advantages and disadvantages.

Section 2: Using os.path 
The os.path module in Python provides useful functions for working with file paths. The join() function can be used to join the parent directory with the current directory. For example:

```
import os
current_dir = os.getcwd()
parent_dir = os.path.join(current_dir, '..')
print(parent_dir)
```

The output will be the parent directory location. The disadvantage of this method is that it only works if the current working directory is known.

Section 3: Using pathlib 
The pathlib module in Python provides an object-oriented way of working with file paths. The parent attribute can be used to get the parent directory. For example:

```
from pathlib import Path
current_dir = Path.cwd()
parent_dir = current_dir.parent
print(parent_dir)
```

The output will be the parent directory location. The advantage of this method is that it works regardless of the current working directory.

Section 4: Using os.pardir 
The os module in Python provides the constant os.pardir, which represents the parent directory. This constant can be used with the join() function to get the parent directory location. For example:

```
import os
parent_dir = os.path.join(os.getcwd(), os.pardir)
print(parent_dir)
```

The output will be the parent directory location. The disadvantage of this method is that it only works if the current working directory is known.

Section 5: Using os.path.dirname 
The os.path module in Python provides the dirname() function, which can be used to get the parent directory location. For example:

```
import os
current_dir = os.getcwd()
parent_dir = os.path.dirname(current_dir)
print(parent_dir)
```

The output will be the parent directory location. The disadvantage of this method is that it only works if the current working directory is known.

Section 6: Conclusion 
This tutorial covered four different methods to get the parent directory location in Python. The choice of method depends on the requirements of the specific application. If the current working directory is known, os.path and os.pardir can be used. If the current working directory is not known, pathlib and os.path.dirname can be used.
