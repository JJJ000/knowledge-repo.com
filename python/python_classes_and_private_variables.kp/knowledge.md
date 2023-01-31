---
title: Is there a way to create private variables in Python classes?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: No, Python does not have private variables in classes.
---

**Contents**

[TOC]

##Yes
Python does have "private" variables in classes. The concept of private variables in Python is implemented through the use of name mangling. Name mangling is the technique of prefixing the name of a variable with a single or double underscore. This is done to indicate that the variable is meant to be private, and should not be accessed directly from outside the class. 

##Name Mangling
Name mangling is done by adding the underscore character (_) to the beginning of the variable name. This tells the interpreter that the variable is private and should not be accessed directly from outside the class. The interpreter then changes the name of the variable to a longer, mangled version. This mangled version is then used internally when accessing the variable. 

##Accessing Private Variables
Private variables can still be accessed from outside the class, but it requires using a special syntax. This syntax involves using the double underscore character (__) followed by the name of the variable. This syntax tells the interpreter to use the mangled version of the variable name, allowing access to the private variable. 

##Example
For example, consider the following code: 

```
class MyClass: 
  def __init__(self): 
    self.__private_var = "This is a private variable"

my_obj = MyClass()
print(my_obj.__private_var)
```

This code will result in an error, since the private variable is not accessible directly from outside the class. To access the private variable, the following syntax must be used: 

```
print(my_obj._MyClass__private_var)
```

This syntax tells the interpreter to use the mangled version of the variable name, allowing access to the private variable.
