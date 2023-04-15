---
title: Can variables, functions, and other created elements be removed from the interpreter's memory?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Yes, it is possible to delete variables, functions, and other objects from the memory of the interpreter using the del keyword.
---

**Contents**

[TOC]

Yes, it is possible to delete created variables, functions, etc from the memory of the interpreter in Python. Here's how:

### Method 1: Using del keyword

The `del` keyword in Python allows us to delete objects from the memory. We can use this keyword to delete variables, lists, dictionaries, functions, etc. For example:

```python
a = 10   # create a variable
del a    # delete the variable
```

### Method 2: Using exec() function

The `exec()` function in Python allows us to execute a string as code. We can use this function to delete an object based on its name stored in a string. For example:

```python
a = 10     # create a variable
exec("del "+ "a")     # delete the variable using its name as a string
```

### Method 3: Using vars() and globals() functions

The `vars()` function in Python returns a dictionary containing the local namespace. The `globals()` function returns a dictionary containing the global namespace. We can use these functions to delete objects based on their name. For example:

```python
a = 10     # create a variable
vars().pop("a")      # delete the variable using vars() function
globals().pop("a")   # delete the variable using globals() function
```

### Method 4: Using reload() function

The `reload()` function in Python can be used to reload a module dynamically. We can use this function to delete objects created by a module. For example:

```python
import mymodule   # import a module

# create an object using the module
obj = mymodule.MyClass()

# delete the object
del obj

# reload the module to delete all its objects
reload(mymodule)
```

Note that the `reload()` function is not available in Python 3.x. In Python 3.x, the `importlib` module provides the `reload()` function.
