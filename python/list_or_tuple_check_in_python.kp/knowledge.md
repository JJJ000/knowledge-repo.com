---
title: Check whether a variable is a list or a tuple
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the isinstance() function to test if a variable is a list or tuple in Python, for example isinstance(my\_var, (list, tuple)).
---

**Contents**

[TOC]

Header: Introduction

Python has different built-in data types, including lists and tuples. Both data types are used to store a collection of values in a single variable. Sometimes we need to check whether a given variable is a list or tuple. In this tutorial, we will learn how to test if a variable is a list or tuple in Python.

Header: Using the isinstance() function

The easiest way to test if a variable is a list or tuple in Python is by using the isinstance() function. The function returns True if the specified variable is an instance of the specified class, otherwise False. 

Here is an example code to check if a variable is a list using the isinstance() function:

```
my_list = [1, 2, 3]

if isinstance(my_list, list):
    print("my_list is a list")
else:
    print("my_list is not a list")
```

The output of this code will be:

```
my_list is a list
```

Similarly, we can use the isinstance() function to check if a variable is a tuple. Here is an example:

```
my_tuple = (1, 2, 3)

if isinstance(my_tuple, tuple):
    print("my_tuple is a tuple")
else:
    print("my_tuple is not a tuple")
```

The output of this code will be:

```
my_tuple is a tuple
```

Header: Using type() function

Another way to test if a variable is a list or tuple in Python is by using the type() function. The type() function returns the type of the specified variable. 

Here is an example code to check if a variable is a list using the type() function:

```
my_list = [1, 2, 3]

if type(my_list) is list:
    print("my_list is a list")
else:
    print("my_list is not a list")
```

The output of this code will be:

```
my_list is a list
```

Similarly, we can use the type() function to check if a variable is a tuple. Here is an example:

```
my_tuple = (1, 2, 3)

if type(my_tuple) is tuple:
    print("my_tuple is a tuple")
else:
    print("my_tuple is not a tuple")
```

The output of this code will be:

```
my_tuple is a tuple
```

Header: Conclusion

In this tutorial, we learned how to test if a variable is a list or tuple in Python. We can use the isinstance() function or the type() function to perform this check. Both methods are simple and easy to use. Using these methods, we can ensure that our program is handling the correct data types.
