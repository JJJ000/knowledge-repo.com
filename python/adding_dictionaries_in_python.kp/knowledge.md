---
title: Add a dictionary to another dictionary
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: You can add a dictionary to a dictionary by using the update() method.
---

**Contents**

[TOC]

### Adding a Dictionary to a Dictionary

The syntax for adding a dictionary to a dictionary is as follows:

```
dict1.update(dict2)
```

Where `dict1` is the dictionary to which you are adding and `dict2` is the dictionary you are adding.

### Example

For example, let's say we have two dictionaries:

```
dict1 = {'a':1, 'b':2}
dict2 = {'c':3, 'd':4}
```

We can add `dict2` to `dict1` like this:

```
dict1.update(dict2)
```

The result is a single dictionary containing all the elements of both `dict1` and `dict2`:

```
{'a':1, 'b':2, 'c':3, 'd':4}
```

### Merging Dictionaries

It is also possible to merge two dictionaries together using the `update()` method. This is done by passing a dictionary as an argument to the `update()` method.

For example, let's say we have two dictionaries:

```
dict1 = {'a':1, 'b':2}
dict2 = {'c':3, 'd':4}
```

We can merge `dict2` into `dict1` using the `update()` method:

```
dict1.update(dict2)
```

The result is a single dictionary containing all the elements of both `dict1` and `dict2`:

```
{'a':1, 'b':2, 'c':3, 'd':4}
```
