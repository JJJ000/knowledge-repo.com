---
title: In python, which one is superior del or delattr?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: The answer is It depends on what you want to achieve - del is used to delete an object or a variable while delattr is used to delete an attribute of an object.
---

**Contents**

[TOC]

Introduction:

In Python, there are different ways to delete an object or attribute from a class or instance. Two of those methods are `del` and `delattr()`. In this article, we will discuss the differences between the two and which one is better.

Comparison of del and delattr:

1. Functionality:

The `del` statement is a built-in Python statement that can remove an object, attribute, or variable from memory. On the other hand, `delattr()` is a built-in Python function that can delete an attribute of an object.

2. Usage:

The `del` statement can be used to remove an object completely or remove a single attribute from an object. It is used as follows:

```python
# Remove an entire object:
del my_object

# Remove an attribute from an object:
del my_object.my_attribute
```

`delattr()` method can only be used to remove an attribute from an object. It is used as follows:

```python
delattr(my_object, "my_attribute")
```

3. Error handling:

The `delattr()` method raises an `AttributeError` if the attribute does not exist in the object. On the other hand, the `del` statement does not raise an error if the attribute does not exist.

4. Readability:

The `del` statement is more readable and concise than the `delattr()` method. It is also the standard way of deleting objects and attributes in Python.

Conclusion:

Both `del` and `delattr()` can be used to delete attributes from objects. However, `del` is more versatile since it can delete an entire object or a single attribute. It is also more readable and concise compared to `delattr()`. Therefore, `del` is the better option in Python.
