---
title: What is the process for unloading (reloading) a Python module?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: To unload (reload) a Python module, use the `importlib.reload()` function.
---

**Contents**

[TOC]

### Unloading a Python Module
1. Use the `del` keyword to unload the module.
2. Pass the module name as an argument to the `del` keyword.

### Example
```python
import mymodule

# Unload the module
del mymodule
```

### Reloading a Python Module
1. Use the `importlib.reload()` function.
2. Pass the module name as an argument to the `importlib.reload()` function.

### Example
```python
import mymodule
import importlib

# Reload the module
importlib.reload(mymodule)
```
