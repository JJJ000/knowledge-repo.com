---
title: Bring in a file from a subfolder?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: To import a file from a subdirectory in Python, use the `from directory import file` syntax.
---

**Contents**

[TOC]

#1. Setting up the Subdirectory

First, you need to create the subdirectory in the same folder as your Python file. To do this, you can use the os module in Python. 

```
import os
os.mkdir('subdirectory')
```

#2. Moving the File

Once the subdirectory has been created, you can move the file you want to import into it. This can be done using the shutil module in Python. 

```
import shutil
shutil.move('file_to_import.txt', 'subdirectory/')
```

#3. Importing the File

Now that the file has been moved to the subdirectory, you can import it into your Python file. To do this, you need to specify the path of the file relative to the Python file. 

```
with open('subdirectory/file_to_import.txt', 'r') as f:
    data = f.read()
```

#4. Cleaning Up

Once the file has been imported, you can delete the subdirectory to clean up the file system. This can be done using the os module in Python. 

```
import os
os.rmdir('subdirectory')
```
