---
title: Using the Python string.join() method on an object array rather than a string array
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: No, string.join() cannot be used on an object array; it can only be used on a string array.
---

**Contents**

[TOC]

**Section 1: Overview**

The `string.join()` method is a built-in Python function that can be used to join a list of strings into a single string, with each item in the list separated by a given separator. It can also be used to join a list of objects, such as integers, floats, and other objects. However, when using `string.join()` on an object array, it is important to note that the resulting string will not contain the object values themselves, but rather their string representations.

**Section 2: Syntax**

The syntax for using `string.join()` on an object array is as follows:

```
string.join(list_of_objects, separator)
```

Where `list_of_objects` is the list of objects to be joined, and `separator` is the string to be used to separate the objects.

**Section 3: Example**

For example, consider the following list of objects:

```
list_of_objects = [1, 2.5, 'three']
```

We can use `string.join()` to join these objects into a single string, with each item separated by a comma:

```
string.join(list_of_objects, ',')
```

This will result in the following string:

```
'1,2.5,three'
```

**Section 4: Considerations**

It is important to note that when using `string.join()` on an object array, the resulting string will not contain the object values themselves, but rather their string representations. For example, the list of objects in the example above will be joined into a string that contains the string representations of the objects (i.e. `'1'`, `'2.5'`, and `'three'`), rather than the objects themselves (i.e. `1`, `2.5`, and `'three'`).
