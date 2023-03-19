---
title: Is it a language guarantee or just an implementation detail that false is equivalent to 0 and true is equivalent to 1?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: It is guaranteed by the language in Python that False == 0 and True == 1.
---

**Contents**

[TOC]

Background
----------

In Python, there are two built-in Boolean values: `True` and `False`. Booleans are often used in conditional statements, loops, and other control structures. But since they ultimately represent some kind of truth value, they can also be used in arithmetic and other operations as a way of representing `1` and `0`, respectively.

So what happens when we try to compare these values to actual integers? Is `True` equivalent to `1`, and is `False` equivalent to `0`? In this answer, we'll explore this question in more depth and see whether this behavior is a guaranteed feature of the Python language or not.

The Answer
----------

The short answer is: yes, `True` is equivalent to `1`, and `False` is equivalent to `0` in Python. This behavior is not an implementation detail, but rather a guaranteed feature of the language itself. Let's dive into why.

Boolean as a subclass of Int
----------------------------

In Python, `bool` is actually a subclass of `int`. This means that boolean values are in fact a special case of integers, and have some of the same behavior as integers. Here's a quick example to demonstrate this:

```
>>> isinstance(True, int)
True
>>> isinstance(False, int)
True
>>> True + True
2
>>> False + False
0
>>> True * 2
2
>>> False * 2
0
```

As you can see, we can perform arithmetic operations like addition and multiplication on booleans just like we can with integers, and the results are what we would expect if `True` were equivalent to `1` and `False` were equivalent to `0`.

Boolean as a singleton
----------------------

Another important aspect of booleans in Python is that they are treated as singletons, meaning that there is only ever one instance of `True` and one instance of `False` in memory. This can have some interesting consequences when comparing boolean values to other types of values, as we'll see in a moment.

```
>>> a = True
>>> b = True
>>> a is b
True
>>> c = 1
>>> d = True
>>> c is d
False
>>> e = False
>>> f = 0
>>> e is f
False
```

As you can see, when we compare two boolean values to each other using the `is` operator, we get `True`, because they are actually the same object in memory. But if we compare a boolean to an integer, even one that has the same value, we get `False`, because they are not the same object in memory.

Comparison to integer literals
-------------------------------

So what about comparing boolean values to integer literals? Is `True` equal to `1`, and is `False` equal to `0`? The answer is yes, and this is guaranteed behavior in Python.

```
>>> True == 1
True
>>> False == 0
True
>>> True != 1
False
>>> False != 0
False
```

As you can see, when we compare `True` to `1`, we get a `True` value, and the same is true for `False` and `0`. This behavior is not an implementation detail, but rather a guaranteed feature of the Python language itself.

Conclusion
----------

In summary, `True` is equivalent to `1`, and `False` is equivalent to `0` in Python. This behavior is not an implementation detail, but rather a guaranteed feature of the language itself, due to the fact that booleans are a subclass of integers and are treated as singletons. This can be useful in certain situations where we want to use booleans in arithmetic or other operations, and it's important to be aware of this behavior when working with Python.
