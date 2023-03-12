---
title: What is the process for altering values in a tuple?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Tuples are immutable, so it is not possible to change the values in a tuple.
---

**Contents**

[TOC]

## Section 1: Introduction
A tuple in Python is an immutable sequence of elements, i.e., once a tuple is created, it cannot be modified. However, there are a few workarounds that allow users to change values inside a tuple. In this tutorial, we will explore these methods in detail.

## Section 2: Unpacking and repacking
One way to change the values inside a tuple is to unpack it and then repack it with the new values. For example:

```python
t = (1, 2, 3, 4)
a, b, c, d = t
t = (a, b, 5, d)
print(t) # Output: (1, 2, 5, 4)
```

In this example, we first unpacked the tuple `t` into four variables `a`, `b`, `c`, and `d`. Then, we created a new tuple with the same values as `t` except for the third value which we changed to 5. Finally, we assigned `t` to the new tuple.

## Section 3: Using lists
Another approach to change the values inside a tuple is to convert it to a list, update the values, and then convert it back to a tuple. Here is an example:

```python
t = (1, 2, 3, 4)
l = list(t)
l[2] = 5
t = tuple(l)
print(t) # Output: (1, 2, 5, 4)
```

In this example, we first converted the tuple `t` to a list `l`. Then, we changed the third value of the list to 5. Finally, we converted the list back to a tuple and assigned it to `t`.

## Section 4: Conclusion
In this tutorial, we have explored two ways to change the values inside a tuple in Python. Although tuples are immutable, these workarounds allow us to modify their elements. However, it is important to note that these methods create new tuples and do not modify the original ones.
