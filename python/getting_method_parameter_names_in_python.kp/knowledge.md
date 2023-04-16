---
title: What are the names of the parameters in the method?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The inspect module can be used to get method parameter names in Python.
---

**Contents**

[TOC]

### Section 1: Using the inspect module

The [inspect module](https://docs.python.org/3/library/inspect.html) provides several useful functions to help get information about live objects such as modules, classes, methods, functions, tracebacks, frame objects, and code objects. To get the parameters of a method, the inspect.signature() function can be used. This function takes a callable object as an argument and returns a Signature object, which contains information about the parameters of the given callable object.

### Section 2: Example

The following example shows how to use the inspect.signature() function to get the parameter names of a method.

```python
import inspect

def my_method(a, b, c):
    pass

sig = inspect.signature(my_method)
params = sig.parameters

# Print the parameter names
for name, param in params.items():
    print(name)

# Output:
# a
# b
# c
```

### Section 3: Using the _ _code_ _ attribute

Another way to get the parameter names of a method is to use the _ _code_ _ attribute. This attribute returns a code object which contains information about the method such as the parameter names, the number of local variables, etc.

### Section 4: Example

The following example shows how to use the _ _code_ _ attribute to get the parameter names of a method.

```python
def my_method(a, b, c):
    pass

code = my_method.__code__
params = code.co_varnames

# Print the parameter names
for name in params:
    print(name)

# Output:
# a
# b
# c
```
