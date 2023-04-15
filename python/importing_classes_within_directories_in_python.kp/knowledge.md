---
title: What is the process for importing a class from within the same directory or a subdirectory?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-30 00:00:00
updated_at: 2023-04-30 00:00:00
tldr: Use the `from <directory>.<file> import <class>` syntax to import the class within the same directory or sub directory in Python.
---

**Contents**

[TOC]

# Section 1: Importing Classes Within the Same Directory 

In Python, you can import classes within the same directory using the `import` statement. This statement will allow you to import any class that is stored in the same directory as your current file. For example, if you have a file called `my_class.py` in the same directory as your current file, you can import it with the following statement: 

```python
import my_class
```

# Section 2: Importing Classes in a Subdirectory 

If you want to import a class that is stored in a subdirectory of your current directory, you can use the `from` statement. This statement will allow you to specify the exact location of the class that you want to import. For example, if you have a file called `my_class.py` stored in the `subdir` subdirectory, you can import it with the following statement: 

```python
from subdir import my_class
```

# Section 3: Importing All Classes in a Directory 

If you want to import all of the classes in a directory, you can use the `import *` statement. This statement will allow you to import all of the classes in a directory with a single statement. For example, if you have a directory called `subdir` with multiple files, you can import all of the classes in that directory with the following statement: 

```python
from subdir import *
```

# Section 4: Importing Specific Classes in a Directory 

If you only want to import specific classes in a directory, you can use the `from` statement with a comma-separated list of class names. This statement will allow you to specify which classes you want to import from a directory. For example, if you have a directory called `subdir` with multiple files, you can import only the `my_class` and `my_other_class` classes with the following statement: 

```python
from subdir import my_class, my_other_class
```
