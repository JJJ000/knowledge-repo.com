---
title: The list in Python is modified based on its value and not based on its reference
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Python lists are passed by reference, but to create a new list with the same values as the original, you can use slicing or the list() constructor.
---

**Contents**

[TOC]

Section 1: Understanding Mutable and Immutable Objects in Python

In Python, objects can be categorized as mutable or immutable. Mutable objects can be changed after they are created, while immutable objects cannot. Examples of mutable objects in Python include lists, sets, and dictionaries, while examples of immutable objects include integers, strings, and tuples.

When a variable is assigned to a mutable object, any changes made to that object will also affect the variable. This is because the variable is pointing to the same object in memory. On the other hand, when a variable is assigned to an immutable object, any changes made to that object will not affect the variable, as a new object will be created in memory.

Section 2: Creating a List by Value in Python

To create a new list by value in Python, you can use the slicing operator. This creates a new object in memory, rather than referencing the original list.

For example:

```
my_list = [1, 2, 3]
new_list = my_list[:] # creates a new list by value
```

In this example, `new_list` is a new object in memory that has the same values as `my_list`. Any changes made to `new_list` will not affect `my_list`, as they are separate objects.

Section 3: Manipulating a List by Value in Python

Once you have created a new list by value in Python, you can manipulate it without affecting the original list. For example, you can append a new value to `new_list`:

```
new_list.append(4)
```

This will add the value `4` to the end of `new_list`, without affecting `my_list`.

Section 4: Conclusion

In Python, it is possible to create a new list by value rather than by reference. This can be achieved by using the slicing operator to create a new object in memory. Manipulating this new list will not affect the original list, as they are separate objects. Understanding the difference between mutable and immutable objects is important when working with lists in Python.
