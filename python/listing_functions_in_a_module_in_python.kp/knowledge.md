---
title: What is the process for displaying all the functions in a module?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: You can use the dir() function to list all functions in a module in Python.
---

**Contents**

[TOC]

# Section 1: Using dir()
Python provides the `dir()` function to list all the functions in a module.

Syntax:
```
dir(module_name)
```

Example:
```
dir(math)
```

# Section 2: Using help()
The `help()` function can be used to list all the functions in a module.

Syntax:
```
help(module_name)
```

Example:
```
help(math)
```

# Section 3: Using __dict__
The `__dict__` attribute of a module can be used to list all the functions in a module.

Syntax:
```
module_name.__dict__
```

Example:
```
math.__dict__
```

# Section 4: Using inspect
The `inspect` module provides the `getmembers()` function which can be used to list all the functions in a module.

Syntax:
```
inspect.getmembers(module_name)
```

Example:
```
inspect.getmembers(math)
```
