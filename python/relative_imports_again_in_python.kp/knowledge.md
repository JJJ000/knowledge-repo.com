---
title: Discussing relative imports once again
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Relative imports allow a module to import other modules located in the same directory as the module being imported.
---

**Contents**

[TOC]

# Overview

Relative imports are used to specify the location of modules relative to the current module, rather than using their full path. This allows for more concise and maintainable code, as well as avoiding the need for absolute paths.

# Syntax

Relative imports use the `from . import` syntax. The period (.) refers to the current directory, and the import statement is followed by the name of the module to be imported.

# Example

For example, suppose we have a module named `my_module.py` in the current directory. To import this module, we would use the following syntax:

```python
from . import my_module
```

# Limitations

Relative imports are limited to modules within the same directory or subdirectories. Absolute imports (using the full path) must be used for modules outside this scope.
