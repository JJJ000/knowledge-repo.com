---
title: The most efficient way to delete a file that may not exist in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the `os.remove` function within a `try-except` block.
---

**Contents**

[TOC]

### Try/Except

The most pythonic way to delete a file which may not exist is to use a try/except block. This will allow the code to attempt to delete the file, and if the file does not exist, it will not raise an error.

```python
try:
    os.remove('path/to/file.ext')
except FileNotFoundError:
    pass
```

### os.path.exists

Another pythonic way to delete a file which may not exist is to first check if the file exists using the os.path.exists method. If the file exists, then delete it.

```python
if os.path.exists('path/to/file.ext'):
    os.remove('path/to/file.ext')
```

### Pathlib

The third pythonic way to delete a file which may not exist is to use the Pathlib module. This module allows the code to check if the file exists and delete it in one line.

```python
Path('path/to/file.ext').unlink(missing_ok=True)
```

### shutil

The fourth and final pythonic way to delete a file which may not exist is to use the shutil module. This module allows the code to check if the file exists and delete it in one line.

```python
shutil.rmtree('path/to/file.ext', ignore_errors=True)
```
