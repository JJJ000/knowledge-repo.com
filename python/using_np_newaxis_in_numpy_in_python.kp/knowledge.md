---
title: What is the purpose of np.newaxis?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: np.newaxis can be used to add a new axis to an existing array in Python.
---

**Contents**

[TOC]

#1 Introduction

np.newaxis is an alias for None, which is used to increase the dimension of an array by one more dimension, when used once. It can be used to expand the shape of an array in any position.

#2 Examples

Example 1:

```
import numpy as np
a = np.array([1,2,3])
print(a.shape)

# Output
(3,)
```

Using np.newaxis, the shape of the array can be changed:

```
b = a[np.newaxis]
print(b.shape)

# Output
(1,3)
```

Example 2:

```
a = np.array([[1,2,3], [4,5,6]])
print(a.shape)

# Output
(2,3)
```

Using np.newaxis, the shape of the array can be changed:

```
b = a[:, np.newaxis]
print(b.shape)

# Output
(2,1,3)
```

#3 Advantages

- np.newaxis is useful when you want to add a new axis to an existing array to perform operations such as broadcasting.
- It allows you to manipulate the shape of an array without changing its data.

#4 Disadvantages

- np.newaxis can be difficult to understand and use correctly.
- It can be inefficient as it requires copying the data from the original array.
