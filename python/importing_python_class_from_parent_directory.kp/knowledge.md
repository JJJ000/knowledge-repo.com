---
title: What is the process for importing a Python class that exists in a directory above?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the syntax `from .. import ClassName` to import a Python class that is in a directory above.
---

**Contents**

[TOC]

# Overview

When working with Python, you may want to import a class that is in a directory above your current directory. This is a common scenario when organizing a larger project. In this tutorial, we will look at how to import a Python class that is in a directory above.

# Solution

The solution to importing a Python class that is in a directory above is to use relative imports. There are a few ways to do this, so let's explore some of them.

## Method 1: sys.path.append

One way to import a Python class that is in a directory above is to use sys.path.append. This method allows you to add a path to your Python path, meaning that Python will look in that directory for modules.

Here is an example:

```python
import sys
sys.path.append('../')
from my_module import MyClass
```

In this example, we first add the parent directory to the Python path using sys.path.append. Then, we can import the class MyClass from the module my_module that is in the parent directory.

## Method 2: Absolute import

Another way to import a Python class that is in a directory above is to use an absolute import. To do this, you need to specify the entire path to the module, starting from the root directory.

Here is an example:

```python
from my_project.my_module import MyClass
```

In this example, we are importing the class MyClass from the module my_module that is in the directory my_project, which is in the root directory.

## Method 3: Relative import

Finally, you can use a relative import to import a Python class that is in a directory above. To do this, you need to use a dot (.) to signify the current directory, and two dots (..) to signify the parent directory.

Here is an example:

```python
from ..my_module import MyClass
```

In this example, we are importing the class MyClass from the module my_module that is in the parent directory.

# Conclusion

In conclusion, there are a few ways to import a Python class that is in a directory above. You can use sys.path.append, an absolute import, or a relative import. The method you choose will depend on your project and personal preferences.
