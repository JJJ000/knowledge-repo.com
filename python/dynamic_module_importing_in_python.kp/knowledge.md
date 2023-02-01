---
title: What is the process for importing a module using its name as a string?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: You can use the built-in function `\_\_import\_\_` to import a module dynamically given its name as a string.
---

**Contents**

[TOC]

## Using importlib

The `importlib` module provides the `import_module` function which can be used to import a module given its name as a string. 

```python
import importlib

# Import a module given its name as a string
module = importlib.import_module("mymodule")
```

## Using __import__

The `__import__` function can also be used to import a module given its name as a string. 

```python
# Import a module given its name as a string
module = __import__("mymodule")
```

## Using exec

The `exec` statement can also be used to import a module given its name as a string. 

```python
# Import a module given its name as a string
exec("import mymodule")
```

## Using sys.modules

The `sys.modules` dictionary can also be used to import a module given its name as a string. 

```python
import sys

# Import a module given its name as a string
module = sys.modules["mymodule"]
```
