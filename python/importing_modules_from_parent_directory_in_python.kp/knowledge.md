---
title: Bringing in libraries from the higher-level directory
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Use the `sys.path.append` function to add the parent folder to the system path, allowing modules from the parent folder to be imported.
---

**Contents**

[TOC]

# Section 1: Setting up the Environment

To allow Python to find modules in a parent folder, you must set up the environment by modifying the sys.path variable. This variable contains the list of directories which Python searches for modules.

# Section 2: Adding the Parent Folder

To add the parent folder to the sys.path variable, you can use the `sys.path.append()` method. This method takes a string argument which contains the path to the parent folder.

# Section 3: Importing Modules

Once the parent folder is added, you can import modules from it by using the `import` keyword. For example, if the parent folder contains a module called `mymodule`, you can import it with the following command:

```python
import mymodule
```

# Section 4: Example

To illustrate, here is an example of how to import a module from a parent folder in Python:

```python
import sys
sys.path.append('../')
import mymodule
```
