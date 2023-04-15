---
title: What is the process for dynamically importing a module using its full path?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the `importlib.import\_module` function to import a module dynamically given the full path in Python.
---

**Contents**

[TOC]

## Using `importlib`

The `importlib` module provides an API for loading and reloading modules. It can be used to import modules given the full path.

```python
import importlib.util

# Load the module from a file
spec = importlib.util.spec_from_file_location("module_name", "/path/to/module.py")
module = importlib.util.module_from_spec(spec)
spec.loader.exec_module(module)
```

## Using `__import__`

The `__import__` function can be used to import a module given its full path.

```python
module = __import__("/path/to/module.py")
```

## Using `imp`

The `imp` module provides an API for importing modules. It can be used to import a module given its full path.

```python
import imp

module = imp.load_source("module_name", "/path/to/module.py")
```

## Using `sys.path`

The `sys.path` variable can be used to add the directory containing the module to the system path. This allows the module to be imported using its name.

```python
import sys

sys.path.append("/path/to/module_dir")
module = import module_name
```
