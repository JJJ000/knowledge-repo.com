---
title: Can you express the concept of 'pointers' in Python differently?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Python has pointers, but they are implicit and automatically handled by the interpreter.
---

**Contents**

[TOC]

Pointers in Python

In Python, there is no concept of pointers like in languages such as C or C++. However, there are ways to simulate pointers or similar functionality using various built-in data types and libraries.

1. References

In Python, variables are actually references to objects, not the objects themselves. This means that when a variable is assigned to an object, it actually points to the object in memory. Therefore, references behave like pointers to the objects they reference.

For example, consider the following code:

```
a = [1, 2, 3]
b = a
b.append(4)
print(a)
```

In this code, `a` and `b` both point to the same list object in memory. When `b` is modified by adding `4` to the list, `a` is also modified since it points to the same object. The output of the code is `[1, 2, 3, 4]`.

2. Pointers through ctypes

The ctypes library in Python provides a way to work with C code and types directly in Python. This library includes a `pointer` type that can be used to simulate pointers to variables.

For example, consider the following code:

```
import ctypes

a = ctypes.c_int(5)
b = ctypes.pointer(a)
print(b.contents)
b.contents = ctypes.c_int(6)
print(a.value)
```

In this code, `a` is an integer variable with the value `5`. `b` is a pointer to `a` created using the `pointer` function from ctypes. The `contents` attribute of `b` is used to access the value pointed to by `b`, which is `5` in this case. We then change the value pointed to by `b` to `6`, which changes the value of `a` since `b` is pointing to `a`. The output of the code is `5` for the first print statement, and `6` for the second print statement.

3. Pointers through numpy arrays

The numpy library in Python provides a way to work with arrays efficiently and perform various numerical operations on them. One of the features of numpy is the ability to create a "view" of an array, which behaves like a pointer to the underlying data.

For example, consider the following code:

```
import numpy as np

a = np.array([1, 2, 3])
b = a.view()
b[0] = 4
print(a)
```

In this code, `a` is an array with the values `[1, 2, 3]`. `b` is created using the `view` function, which creates a view of `a`. The first element of `b` is then changed to `4`. Since `b` is a view of `a`, this also changes the value of the first element of `a` to `4`. The output of the code is `[4, 2, 3]`.

4. Conclusion

While Python does not have pointers in the traditional sense like C or C++, there are ways to simulate pointer behavior using references, the ctypes library, and the numpy library. These techniques can be useful for certain applications and are worth exploring.
