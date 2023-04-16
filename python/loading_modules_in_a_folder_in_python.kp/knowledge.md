---
title: What is the procedure for importing all modules in a directory?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the `importlib.import\_module` function to import all modules in a folder.
---

**Contents**

[TOC]

# Section 1: Import os Module

In order to load all modules in a folder, the first step is to import the os module. The os module provides a portable way of using operating system dependent functionality.

# Section 2: List Modules in Folder

The next step is to list the modules in the folder. This can be done using the os.listdir() method. This method returns a list containing the names of the entries in the directory given by path.

# Section 3: Import Module

Once the modules in the folder have been listed, the modules can be imported one by one using the import command. For example, if there is a module named "my_module.py" in the folder, it can be imported using the following command:

```
import my_module
```

# Section 4: Iterate Through List of Modules

Finally, the list of modules can be iterated through and each module can be imported. This can be done using a for loop. For example:

```
for module in os.listdir('my_folder'):
    import module
```
