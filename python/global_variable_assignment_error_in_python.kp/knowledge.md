---
title: An unboundlocalerror occurs when attempting to utilize a variable, which was deemed global, but is later reassigned after its initial use
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: You need to declare the variable as global inside the function where it is being (re)assigned.
---

**Contents**

[TOC]

Introduction

In Python, variables can be defined and used within different scopes, such as global or local. Variables defined outside a function, for instance, are called global variables and can be accessed and modified from within the function scope. However, if a local variable with the same name as a global variable is defined within the function, any changes made to it will only apply to that local scope, not the global one. This may lead to the UnboundLocalError.

In this article, we will discuss this error and explore how to resolve it.

What is the UnboundLocalError?

The UnboundLocalError is an exception in Python that is raised when a local variable is referenced before it has been assigned a value, or a variable is assigned a value within a local scope but referenced before it has been assigned in that same scope.

For example, if we define a variable inside a function and try to access it before assigning a value, we will get an UnboundLocalError:

``` python
def my_function():
    print(my_variable)
    my_variable = 42

my_function()
```
Output:

``` python
UnboundLocalError: local variable 'my_variable' referenced before assignment
```

The first line of the function tries to print the value of `my_variable`, but at this point, it has not been assigned a value. Thus, the interpreter raises an UnboundLocalError.

How to resolve the UnboundLocalError

There are several ways to resolve the UnboundLocalError:

1. Use the `global` keyword
The `global` keyword can be used to indicate that a variable is a global variable, not a local one. This way, any changes made to the variable within the function scope will apply to the global variable, as well.

``` python
my_variable = 0

def my_function():
    global my_variable
    print(my_variable)
    my_variable = 42

my_function()
print(my_variable)
```

Output:
```
0
42
```

2. Assign a default value to the variable
If a variable is expected to be used within a function, but may not be initialized under certain conditions, a default value can be assigned to the variable to avoid UnboundLocalError.

``` python
def my_function(condition):
    if condition:
        my_variable = 42
    else:
        my_variable = None
    print(my_variable)

my_function(True)
my_function(False)
```

Output:
``` python
42
None
```

3. Use a different naming convention for local and global variables
One way to avoid conflicts between local and global variables is to use different naming conventions for them. For example, global variables can be named `GLOBAL_VARIABLE`, while local ones can simply be named `variable`.

``` python
GLOBAL_VARIABLE = 0

def my_function():
    variable = 42
    print(GLOBAL_VARIABLE)
    print(variable)

my_function()
print(GLOBAL_VARIABLE)
```

Output:
``` python
0
42
0
```

Conclusion

The UnboundLocalError is a common exception in Python that can occur when a local variable is referenced before it has been assigned. This error can be resolved by using the `global` keyword, assigning a default value to the variable, or using a different naming convention for local and global variables.
