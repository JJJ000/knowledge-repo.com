---
title: Python 2.6 has discontinued the usage of baseexception.message
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Yes, the attribute BaseException.message is deprecated in Python 2.6 and should not be used.
---

**Contents**

[TOC]

Introduction

In Python programming language, BaseException is the root class of all exception classes. It defines common methods for all exception classes such as __str__(), __repr__() and message(). However, in Python 2.6, the message attribute of BaseException class has been deprecated. This means that message attribute can still be used but it is not recommended. Instead, the args attribute should be used to store error message.

Reason for deprecating message attribute

The reason for deprecating message attribute of BaseException class is to simplify exception handling and make it more consistent across all exception classes. In Python, the convention is to store error message in args attribute as a tuple. This tuple may contain one or more elements depending on how many arguments are passed. By doing this, it becomes easier to extract error message from the exception object.

Examples of using args attribute

Let's consider the following examples to demonstrate the use of args attribute for storing error message.

```python
try:
    10/0
except ZeroDivisionError as e:
    print e.args
```

In the above code, a division by zero error is intentionally caused and caught. The error message is stored in e.args attribute which is a tuple containing the error message. When we print e.args, the output is as follows:

```python
('integer division or modulo by zero',)
```

Let's consider another example:

```python
class CustomError(Exception):
    pass
    
try:
    raise CustomError("An error occurred")
except CustomError as e:
    print e.args
```

In the above code, a custom exception is defined by inheriting from Exception class. Then, this exception is raised with an error message. The error message is stored in e.args attribute which is a tuple containing the error message. When we print e.args, the output is as follows:

```python
('An error occurred',)
```

Conclusion

Thus, we can see that in Python 2.6, the message attribute of BaseException class has been deprecated. Instead, args attribute should be used to store error message. This convention makes it easier to extract error message from the exception object and simplifies exception handling.
