---
title: What is the method for determining if a variable is a function?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use the built-in callable() function to detect whether a variable is a function in Python.
---

**Contents**

[TOC]

#Using type()

The type() method is the most straightforward way to detect whether a variable is a function in Python. This method returns the type of the variable passed as an argument. If the variable is a function, the type() method will return 'function'.

Example:
```
def my_func():
    print("Hello World!")

result = type(my_func)
print(result)
```

Output:
```
<class 'function'>
```

#Using isinstance()

The isinstance() method can also be used to detect whether a variable is a function in Python. This method takes two arguments - the variable to be tested and the type to be tested against. If the variable is a function, the isinstance() method will return True.

Example:
```
def my_func():
    print("Hello World!")

result = isinstance(my_func, type(my_func))
print(result)
```

Output:
```
True
```
