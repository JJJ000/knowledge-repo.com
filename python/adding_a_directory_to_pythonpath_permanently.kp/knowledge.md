---
title: How can I permanently add a directory to pythonpath?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The directory can be added to the PYTHONPATH environment variable, which will make it permanently available to Python.
---

**Contents**

[TOC]

**Section 1: Checking the Current PYTHONPATH**

To check what is currently in the PYTHONPATH, you can use the `sys` module to print out the list of paths.

```python
import sys
print(sys.path)
```

**Section 2: Adding a Directory to PYTHONPATH**

To add a directory to the PYTHONPATH, you can use the `sys.path.append()` method.

```python
import sys
sys.path.append('/path/to/directory')
```

**Section 3: Making the Change Permanent**

The change to the PYTHONPATH will only be temporary, so to make it permanent you need to set the `PYTHONPATH` environment variable.

You can do this in the terminal by running the following command:

```bash
export PYTHONPATH=/path/to/directory
```

**Section 4: Verifying the Change**

To verify that the directory has been added successfully to the PYTHONPATH, you can run the same `sys.path` command as before.

```python
import sys
print(sys.path)
```

The directory should now be included in the list of paths.
