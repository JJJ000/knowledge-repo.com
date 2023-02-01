---
title: What is the file path and name of the program that is running?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: The path and name of the currently executing file can be retrieved using the \_\_file\_\_ attribute.
---

**Contents**

[TOC]

# Section 1: Using sys.argv

The sys.argv attribute of the sys module can be used to get the path and name of the file that is currently executing in Python. This attribute is a list of strings containing the command-line arguments passed to the Python script. The first element of this list is the path and name of the file that is currently executing.

# Section 2: Example

The following example demonstrates how to use sys.argv to get the path and name of the file that is currently executing: 

```
import sys

# Get the path and name of the file that is currently executing
file_path_and_name = sys.argv[0]

# Print the file path and name
print(file_path_and_name)
```

# Section 3: Output

The output of the above code will be the path and name of the file that is currently executing.

# Section 4: Conclusion

Using the sys.argv attribute of the sys module, it is possible to get the path and name of the file that is currently executing in Python.
