---
title: In python, retrieve a specific directory from the file path
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: To extract a part of the filepath (a directory) in Python, you can use the os.path module and the split() method.
---

**Contents**

[TOC]

1. Introduction
To extract a part of the file path in Python, we can use various string manipulation functions and modules like os.path.

2. Using os.path module
The os.path module in Python provides many methods that work on pathnames. One of such methods is the os.path.basename() method, which returns the base name of the file path specified in the argument. Here is an example:

```
import os

path = '/home/user/Documents'

dir_name = os.path.basename(path)

print(dir_name)
```

Output:
```
Documents
```

In this example, we have used the os.path.basename() method to extract the last directory name from the given file path.

3. Using string manipulation methods
In addition to the os.path module, we can also use Python string manipulation methods to extract the directory name from a file path. For example, we can use the split() method to split the file path into individual directories and then get the last directory name. Here is an example:

```
path = '/home/user/Documents'

dir_name = path.split('/')[-1]

print(dir_name)
```

Output:
```
Documents
```

In this example, we have used the split() method to split the file path using the '/' separator and then used the [-1] index to get the last directory name.

4. Conclusion
In this tutorial, we have learned two ways to extract a part of the file path (i.e., a directory) in Python. We can use either the os.path module or string manipulation methods to accomplish this task.
