---
title: The process of including a directory in either the sys.path or pythonpath
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can add a directory to sys.path or PYTHONPATH by using the append method of sys.path or by setting the environment variable PYTHONPATH.
---

**Contents**

[TOC]

Section 1: Introduction

In Python, we use the `sys.path` or `PYTHONPATH` variable to import modules from directories that are not in the default search path. We can add paths to the `sys.path` variable or the `PYTHONPATH` environment variable to include additional directories in the search path. In this guide, we will discuss how to add directories to `sys.path` or `PYTHONPATH` in Python.

Section 2: Adding a directory to `sys.path`

To add a directory to `sys.path`, we can use the `sys.path.append()` method. Here is an example:

```python
import sys
sys.path.append('/path/to/directory')
```

This will add the directory `/path/to/directory` to the `sys.path` variable, and modules in that directory can be imported using the `import` statement.

Section 3: Adding a directory to `PYTHONPATH`

To add a directory to the `PYTHONPATH` environment variable, we can use the command line or the operating system's environment variable settings.

On Linux and macOS, we can add directories to the `PYTHONPATH` variable by setting the variable in the terminal session, like this:

```bash
export PYTHONPATH=/path/to/directory:$PYTHONPATH
```

This will prepend the directory `/path/to/directory` to the `PYTHONPATH` variable. The `:$PYTHONPATH` at the end ensures that any existing `PYTHONPATH` value is retained.

On Windows, we can add directories to the `PYTHONPATH` variable using the `setx` command, like this:

```batch
setx PYTHONPATH "%PYTHONPATH%;C:\path\to\directory"
```

This will append the directory `C:\path\to\directory` to the `PYTHONPATH` variable. The `%PYTHONPATH%` ensures that any existing `PYTHONPATH` value is retained.

Section 4: Conclusion

In summary, we can add directories to the `sys.path` variable using the `sys.path.append()` method, and add directories to the `PYTHONPATH` environment variable using command line or operating system settings. By adding directories to `sys.path` or `PYTHONPATH`, we can extend the search path for Python modules and make it easier to organize and distribute Python code.
