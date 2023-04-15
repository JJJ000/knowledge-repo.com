---
title: What makes circular imports appear functional at higher levels in the call stack but eventually result in an importerror at lower levels?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Circular imports can seemingly work further up in the call stack because the modules being imported may have already been initialized, but an ImportError is raised further down because the circular import prevents the second module from being fully initialized.
---

**Contents**

[TOC]

Overview

Circular imports occur when two or more modules import each other indirectly, forming a closed loop. In Python, circular imports can lead to unexpected results, including ImportError exceptions. In this article, we will explore why circular imports seemingly work further up in the call stack but then raise an ImportError further down in Python.

1. Python’s Import Mechanism

Before we dive into circular imports, we need to understand how Python’s import mechanism works. When you import a module, Python creates a new module object and executes the code in that module. Any names defined in the module’s namespace become attributes of the module object. 

2. Circular Imports

Circular imports occur when two or more modules attempt to import each other. For instance, consider the following two files: `file1.py` and `file2.py`.

    # file1.py
    import file2
    
    def hello():
        return "Hello from file1"
        
    print(file2.world())
    
    
    # file2.py
    import file1
    
    def world():
        return "World from file2"
        
    print(file1.hello())

At first glance, it may look like this code should work, but it will actually raise an ImportError exception. This is because when `file1.py` is being imported, Python needs to import `file2.py` as well, since it is used in the `hello()` function. However, when Python starts to import `file2.py`, it also needs to import `file1.py`, since it is used in the `world()` function. This creates a cycle where Python keeps trying to import the same two modules over and over again.

3. Why Circular Imports Raise ImportError Exceptions?

When Python encounters a circular import, it tries to resolve the import by temporarily stopping the execution of the current module until the import is resolved. However, this mechanism has its limits. 

Python only resolves circular imports if it can find a single reference to the module in the namespace of the importing module. When there are more than one references to a module, Python can no longer resolve the import and raises ImportError exceptions.

In our example, `file1.py` and `file2.py` both have references to each other. So when Python tries to resolve the import, it cannot find a single reference, which leads to an ImportError exception.

4. How to Fix Circular Imports

To avoid circular imports, it is recommended to restructure your code. One way to do this is to move the common parts of the code that are used by both modules into a third module. This way, each module can import the third module without creating a circular import.

Another way to avoid circular imports is to refactor your code to minimize the amount of cross-module dependency. You can also use import statements inside functions or methods instead of at the module level, as this can reduce the likelihood of circular imports.

In conclusion, circular imports can lead to unexpected results in Python. It is always a good practice to avoid circular imports or restructure your code to minimize cross-module dependencies.
