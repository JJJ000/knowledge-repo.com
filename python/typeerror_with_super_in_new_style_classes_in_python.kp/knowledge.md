---
title: Calling super() on a new-style class will raise a typeerror, stating that the argument must be a type, not a class object
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The super() function cannot be used with new-style classes in Python because it requires an instance of a type, not a class object.
---

**Contents**

[TOC]

# Introduction

In Python, the super() method is used to refer to the parent class. It is used to access the methods and properties of the parent class from the child class. However, when using the super() method with a new-style class, a TypeError may be raised that says "TypeError: must be type, not classobj". This error can be confusing and can be difficult to debug. In this article, we will discuss the causes of this error and how to fix it.

# Causes of the Error

The error occurs because the super() method is not being used correctly. The super() method is meant to be used with a type, not a class object. A class object is a representation of the class, while a type is a specific instance of the class. 

When the super() method is used with a class object, the interpreter is unable to find the parent class and thus raises the error.

# Fixing the Error

The error can be fixed by using the super() method with a type instead of a class object. To do this, the type needs to be passed as an argument to the super() method. This will allow the interpreter to find the parent class and the error will be avoided.

# Conclusion

The TypeError raised when using the super() method with a new-style class in Python can be confusing and difficult to debug. The error occurs because the super() method is not being used correctly and should be used with a type instead of a class object. By passing a type as an argument to the super() method, the error can be avoided.
