---
title: Is it better to use "import os.path" or "import os"?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: It depends on whether you only need to access functions related to path manipulation (use `import os.path`) or other operating system functions as well (use `import os`).
---

**Contents**

[TOC]

Importing os.path vs os in Python

In Python, there are multiple ways to import modules, and often developers are not sure which one to use. In this article, we will discuss when to use `import os.path` and when to use `import os` in Python.

Understanding os and os.path

The `os` and `os.path` modules in Python provide useful functions to interact with the file system and operating system.

The `os` module provides functions to access the operating system functionality like reading or writing environment variables, getting the current working directory, and listing directories.

The `os.path` module provides functions to handle file and directory paths, like joining paths, splitting paths, and checking if a path exists.

Importing os.path

If you only need to use the functions provided by the `os.path` module, you can import the module directly using `import os.path`. This can save memory and improve performance as only the `os.path` module will be loaded, and not the entire `os` module.

For example, if you only need to check if a file exists, you can use `os.path.exists()`:

```python
import os.path

if os.path.exists('/path/to/file'):
    print('File exists')
else:
    print('File does not exist')
```

Importing os

If you need to use the functions provided by both the `os` and `os.path` modules, it's recommended to import the `os` module using `import os`.

For example, if you need to get the current working directory and check if a file exists, you can use `os.getcwd()` and `os.path.exists()`:

```python
import os

cwd = os.getcwd()
if os.path.exists('/path/to/file'):
    print('File exists')
else:
    print('File does not exist')
```

Summary

In summary, if you only need to use the functions provided by the `os.path` module, it's recommended to import the module directly using `import os.path`. However, if you need to use functions provided by both the `os` and `os.path` modules, it's recommended to import the `os` module using `import os`.
