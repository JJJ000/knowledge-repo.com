---
title: The function call for module.__init__() is provided with three arguments, but it can accept a maximum of two arguments, causing a typeerror
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: When defining a class in Python, make sure to put `self` as the first parameter in the `\_\_init\_\_` method, because it takes one implicit argument, which is the class instance itself.
---

**Contents**

[TOC]

Section 1: Introduction
One common error that Python developers run into is the "TypeError: module.__init__() takes at most 2 arguments (3 given)". This error can be frustrating to deal with, especially if you are new to Python programming. However, the error is relatively easy to fix once you understand what is causing it.

Section 2: Explanation
The "TypeError: module.__init__() takes at most 2 arguments (3 given)" error occurs when you try to initialize a module with more than two arguments. Python modules are initialized by calling the __init__() method, which takes two arguments: self and __name__. The self argument refers to the module object itself while the __name__ argument specifies the name of the module. If you pass in more than two arguments to the __init__() method, you will get the "TypeError: module.__init__() takes at most 2 arguments (3 given)" error.

Section 3: Examples
Here is an example of how this error can occur:

```
# Define a module that takes in three arguments
class MyModule:
def __init__(self, arg1, arg2, arg3):
    self.arg1 = arg1
    self.arg2 = arg2
    self.arg3 = arg3
```

If you try to initialize this module with more than two arguments, you will get the "TypeError: module.__init__() takes at most 2 arguments (3 given)" error:

```
# Try to initialize the module with three arguments
import MyModule
my_module = MyModule("foo", "bar", "baz")
```

To fix this error, you need to modify the module to take in only two arguments:

```
# Define a module that takes in two arguments
class MyModule:
def __init__(self, arg1, arg2):
    self.arg1 = arg1
    self.arg2 = arg2
```

Now you can initialize the module without getting the error:

```
# Initialize the module with two arguments
import MyModule
my_module = MyModule("foo", "bar")
```

Section 4: Conclusion
In conclusion, "TypeError: module.__init__() takes at most 2 arguments (3 given)" is a common error that is caused by trying to initialize a module with more than two arguments. To fix this error, you need to modify the module to take in only two arguments or pass in fewer arguments when initializing the module.
