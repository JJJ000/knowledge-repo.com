---
title: What is the process for obtaining the source code of a Python function?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: You can get the source code of a Python function by using the `inspect` module.
---

**Contents**

[TOC]

# Using the inspect module
The inspect module allows you to access the source code of any Python function. To use this module, you need to import it first.

```python
import inspect
```

Once imported, you can access the source code for any function by using the `inspect.getsource()` function.

```python
source_code = inspect.getsource(function_name)
```

# Using the built-in __source__ attribute
Python functions also have a built-in `__source__` attribute which can be used to access the source code.

```python
source_code = function_name.__source__
```

# Using the built-in __code__ attribute
Python functions also have a built-in `__code__` attribute which can be used to access the source code.

```python
source_code = function_name.__code__.co_source
```

# Using the ast module
The ast module can be used to access the source code of a Python function. To use this module, you need to import it first.

```python
import ast
```

Once imported, you can access the source code for any function by using the `ast.get_source()` function.

```python
source_code = ast.get_source(function_name)
```
