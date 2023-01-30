---
title: What is the best way to delete a folder that contains files?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Use the shutil.rmtree() function to recursively delete a folder and its contents.
---

**Contents**

[TOC]

1. Using shutil.rmtree()
--------------------------------
The shutil module provides a function called `rmtree()` which is used to delete a non-empty directory. It takes the path of the folder to be deleted as an argument.

Example:
```
import shutil
shutil.rmtree("/path/to/folder")
```

2. Using os.removedirs()
--------------------------------
The `os` module provides a function called `removedirs()` which is used to remove a non-empty directory. It takes the path of the folder to be deleted as an argument.

Example:
```
import os
os.removedirs("/path/to/folder")
```

3. Using os.walk()
--------------------------------
The `os` module provides a function called `walk()` which is used to traverse a directory tree and delete all the contents of the directory.

Example:
```
import os
for root, dirs, files in os.walk("/path/to/folder", topdown=False):
   for name in files:
      os.remove(os.path.join(root, name))
   for name in dirs:
      os.rmdir(os.path.join(root, name))
```

4. Using os.system()
--------------------------------
The `os` module provides a function called `system()` which is used to execute a command in the operating system's shell. We can use this function to execute the `rm -rf` command which will delete a non-empty directory.

Example:
```
import os
os.system("rm -rf /path/to/folder")
```
