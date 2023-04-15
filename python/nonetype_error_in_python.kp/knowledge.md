---
title: Python raises a typeerror indicating that nonetype object cannot be iterated
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: This error occurs when you try to iterate over a variable that contains a value of None, which is not iterable.
---

**Contents**

[TOC]

Section 1: Overview
--------------------

This error occurs in Python when you try to iterate over an object that has the value of `None`. In programming, `None` is a special value that represents the absence of a value. In other words, it means that a variable or object has no value assigned to it.


Section 2: Example
-------------------

Here's an example of code that can produce this error:

```python
def get_values():
    # Some code here that retrieves values
    return None

for value in get_values():
    print(value)
```

In this code, the `get_values` function returns `None`. When we try to iterate over the result of this function, we'll get the `TypeError: 'NoneType' object is not iterable` error. This is because `None` is not iterable.


Section 3: Solution
-------------------

To fix this error, we need to make sure that we're iterating over an iterable object. In the example code above, we can fix the issue by returning an empty list instead of `None` from the `get_values` function:

```python
def get_values():
    # Some code here that retrieves values
    return []

for value in get_values():
    print(value)
```

In this updated version of the code, `get_values` returns an empty list instead of `None`. When we iterate over this list, we won't encounter the `TypeError` anymore.


Section 4: Conclusion
---------------------

In conclusion, the `TypeError: 'NoneType' object is not iterable` error occurs when we try to iterate over an object that has the value of `None`. To fix this error, we need to make sure that we're always iterating over an iterable object, such as a list or tuple. When we encounter this error, we should check if we are returning `None` from any functions that are being used in the iteration, and if so, fix them to return an iterable object instead.
