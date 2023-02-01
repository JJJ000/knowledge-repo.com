---
title: Adding items to a dictionary using the Python "extend" method
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: The `extend` method for a dictionary adds the items from one dictionary to another.
---

**Contents**

[TOC]

# Syntax
The syntax for extending a dictionary in Python is as follows:

`dict.update(dict2)`

# Explanation
The `update()` method updates the dictionary with the elements from the specified dictionary object or from an iterable of key/value pairs. This method does not return any value (returns None).

# Example
For example, if we have two dictionaries:

```
dict1 = {'a':1, 'b':2}
dict2 = {'c':3, 'd':4}
```

Then we can extend `dict1` with `dict2` using the `update()` method:

```
dict1.update(dict2)
```

This will update `dict1` with the elements from `dict2` and the result will be:

```
dict1 = {'a':1, 'b':2, 'c':3, 'd':4}
```
