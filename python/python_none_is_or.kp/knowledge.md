---
title: Which should I use for comparing to none in Python "is" or ==?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Use `is` to compare with None, as it checks for object identity, whereas == checks for equality.
---

**Contents**

[TOC]

## Introduction
In Python, `None` is a special object that represents the absence of a value. It is commonly used to indicate that a variable does not have any value or that a function does not return a value. When comparing `None` to another object, you may wonder whether you should use the `is` keyword or the `==` operator. In this article, we will explore the differences and similarities between these two comparison methods and find out when to use each one.

## `is` operator
The `is` operator checks whether two objects are the same object in memory. When you use the `is` operator to compare an object to `None`, it will return `True` if the object is `None`, and `False` otherwise. Here's an example:

```python
x = None
y = None

print(x is None) # True
print(x is y) # True

z = 0

print(z is None) # False
```

In this example, the first two `print` statements return `True` because `x` and `y` are both set to `None`. The third `print` statement returns `False` because `z` is not `None`. 

## `==` operator
The `==` operator checks whether two objects have the same value. When you use the `==` operator to compare an object to `None`, it will return `True` if the object is `None`, and `False` otherwise. Here's an example:

```python
x = None
y = None

print(x == None) # True
print(x == y) # True

z = 0

print(z == None) # False
```

In this example, the first two `print` statements return `True` because `x` and `y` are both set to `None`. The third `print` statement returns `False` because `z` is not `None`. 

## When to use `is` or `==`
Both `is` and `==` can be used to compare an object to `None`, but there are some differences in their behavior that you should be aware of. 

Use `is` when you want to check whether two objects are the same object in memory. This is particularly useful when checking whether a mutable object has been modified, as the `==` operator may return `True` even if the object has been changed. 

Use `==` when you want to check whether two objects have the same value. This is particularly useful when comparing immutable objects, as the `is` operator may return `False` even if the objects have the same value. 

In general, if you're not sure which one to use, it's safer to use `==` unless you're specifically checking for identity. 

## Conclusion
In conclusion, both `is` and `==` can be used to compare an object to `None`, but they have slightly different behavior. Use `is` to check for identity and use `==` to check for value equality. When in doubt, it's safer to use `==` unless you specifically need to check for identity.
