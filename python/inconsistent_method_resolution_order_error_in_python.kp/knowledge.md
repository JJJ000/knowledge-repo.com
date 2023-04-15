---
title: The mro cannot be determined due to a typeerror
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: This error occurs when multiple inherited classes have conflicting method definitions or order.
---

**Contents**

[TOC]

# Introduction

In Python, the Method Resolution Order (MRO) is used to determine the order in which methods or attributes are looked up in a hierarchy of classes. However, sometimes there may be cases where it is not possible to create a consistent MRO. In this article, we will discuss the reasons behind this error and how to solve it. 

# Multiple Inheritance

One of the main reasons for the MRO error is multiple inheritance. When a class inherits from multiple parent classes, Python needs to determine the order in which to look up methods or attributes. There are situations where it is not possible to find a consistent order because of conflicts between the parent classes. For example, consider the following code:

```
class A:
    def foo(self):
        print("A")

class B:
    def foo(self):
        print("B")

class C(A,B):
    pass

class D(B,A):
    pass

```

Here, we have two classes C and D that inherit from classes A and B in different orders. In this case, Python is unable to determine a consistent MRO because there is a conflict between the two parent classes. To solve this problem, we need to use the `super()` function which helps Python to determine a consistent MRO.

# Using the super() function

The `super()` function can be used to call a method from a parent class. This helps to ensure that the MRO is consistent and that the correct method is called. Here is an example:

```
class A:
    def foo(self):
        print("A")

class B:
    def foo(self):
        print("B")

class C(A,B):
    def foo(self):
        super().foo()

class D(B,A):
    def foo(self):
        super().foo()

```

In this example, we have defined a `foo()` method in each class but have used the `super()` function to call the correct method from the parent class. This ensures a consistent MRO and avoids the TypeError.

# Diamond Problem

Another reason for the MRO error is the diamond problem. This occurs when a subclass inherits from two parent classes that have a common ancestor class. For example:

```
class A:
    def foo(self):
        print("A")

class B(A):
    def foo(self):
        print("B")

class C(A):
    def foo(self):
        print("C")

class D(B,C):
    pass

class E(C,B):
    pass

```

Here, we have two classes D and E that inherit from classes B and C, which in turn inherit from class A. In this case, Python is unable to determine a consistent MRO because of the diamond problem. To solve this problem, we can use the `super()` function along with the `MRO` method to determine the correct method order. 

# Conclusion

The MRO error can occur when there are conflicts between parent classes or when there is a diamond problem. Using the `super()` function can help to ensure a consistent MRO and avoid this error. Additionally, we can also use the `MRO` method to determine the correct order of method execution in diamond problem.
