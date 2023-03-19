---
title: Could the 'in' operator of Python be overridden?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: To override Python`s `in` operator, define the \_\_contains\_\_() method in the class.
---

**Contents**

[TOC]

Section 1: Introduction
Python's 'in' operator is primarily used to test whether a given element is present in a sequence (e.g., a list or tuple). However, in some cases, it may be desirable to override the default behavior of the 'in' operator. This can be done by defining custom behavior for the '__contains__()' magic method. In this tutorial, we'll explore how to override the 'in' operator in Python.

Section 2: Defining custom behavior for '__contains__()'
To override the 'in' operator in Python, we need to define custom behavior for the '__contains__()' magic method. This method is called when the 'in' operator is used on an object. By default, '__contains__()' returns True if the given element is present in the object and False otherwise. We can override this behavior by defining our own '__contains__()' method for our object.

Here's an example of how to define custom '__contains__()' behavior for a class:

```python
class MyClass:
    def __init__(self, elements):
        self.elements = elements

    def __contains__(self, element):
        return element in self.elements
```

In this example, we've defined a custom '__contains__()' method for our 'MyClass' object. This method returns True if the given 'element' is present in the 'elements' list and False otherwise.

Section 3: Using the overridden 'in' operator
Once we've defined custom '__contains__()' behavior for our object, we can use the overridden 'in' operator like this:

```python
my_obj = MyClass([1, 2, 3])
print(1 in my_obj)  # Output: True
print(4 in my_obj)  # Output: False
```

In this example, we've created an instance of our 'MyClass' object and passed in the list '[1, 2, 3]' as the 'elements' parameter. We then use the 'in' operator to test whether the elements '1' and '4' are present in the object. As expected, '1' is present in the object and '4' is not.

Section 4: Conclusion
In this tutorial, we've seen how to override Python's 'in' operator by defining custom '__contains__()' behavior for an object. By doing so, we can customize the behavior of the 'in' operator to suit our needs.
