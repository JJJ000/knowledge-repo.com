---
title: Recursively removing directories in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: To delete folders recursively in Python, use the shutil.rmtree() function.
---

**Contents**

[TOC]

# Section 1: Importing Libraries

The `os` and `shutil` libraries must be imported in order to delete folders in Python recursively.

```python
import os
import shutil
```

# Section 2: Creating a Recursive Function

A recursive function must be created to delete the folders recursively. The function should take in the path of the folder as an argument.

```python
def delete_folder_recursively(path):
    for root, dirs, files in os.walk(path, topdown=False):
        for file in files:
            os.remove(os.path.join(root, file))
        for dir in dirs:
            shutil.rmtree(os.path.join(root, dir))
```

# Section 3: Calling the Function

The function can then be called with the path of the folder to be deleted as an argument.

```python
delete_folder_recursively('path/to/folder')
```

# Section 4: Verifying Deletion

The folder can then be verified to be deleted by using the `os.path.exists` method.

```python
if os.path.exists('path/to/folder'):
    print('Folder still exists!')
else:
    print('Folder deleted successfully!')
```
