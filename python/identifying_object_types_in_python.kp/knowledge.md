---
title: Find out what kind of object it is
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The type of an object in Python can be determined using the type() function.
---

**Contents**

[TOC]

#### Type() Function

The type() function is a built-in function in Python that can be used to determine the type of an object. This function takes a single argument and returns the type of the argument.

#### Example

For example, if we want to determine the type of an integer, we can use the type() function as follows:

```
x = 3
type(x)
```

The output of the above code is:

```
<class 'int'>
```

#### Other Ways

In addition to the type() function, Python also provides the isinstance() function, which can be used to determine the type of an object. The isinstance() function takes two arguments, the first argument is the object to check and the second argument is the type to check against.

#### Example

For example, if we want to determine if an integer is an instance of the int type, we can use the isinstance() function as follows:

```
x = 3
isinstance(x, int)
```

The output of the above code is:

```
True
```
