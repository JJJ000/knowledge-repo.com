---
title: Does Python have a built-in identity function?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: Yes, the built-in identity function in Python is called `id()`.
---

**Contents**

[TOC]

Yes, there is a builtin identity function in Python.

### Section 1: What is an identity function?

An identity function is a function that returns the same value that was passed as an argument. In other words, it simply returns the input value without any modification.

### Section 2: The `id()` function

In Python, the `id()` function can be considered as an identity function. It takes an object as an argument and returns a unique identifier for the object. This identifier is guaranteed to be unique and constant for the lifetime of the object.

Example:

```
x = 10
print(id(x))
```

Output:
```
140732070189712
```

In this example, the `id()` function returns a unique identifier for the integer object `10`.

### Section 3: Differences between `id()` and a typical identity function

While `id()` can be considered as an identity function, it has some key differences from a typical identity function:
- `id()` returns the unique identifier for an object, whereas a typical identity function would simply return the input value.
- `id()` always returns an integer value, whereas a typical identity function could potentially return any data type.

### Section 4: Creating a custom identity function

If you want to create your own identity function that simply returns the input value, you can define a function with a single argument that returns that argument.

Example:

```
def identity(x):
    return x

y = 20
print(identity(y))
```

Output:
```
20
```

In this example, the `identity()` function simply returns the input value `y`, which is `20`.
