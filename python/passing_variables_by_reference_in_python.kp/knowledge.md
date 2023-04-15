---
title: What is the process for passing a variable by reference?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: In Python, variables are passed by reference by default.
---

**Contents**

[TOC]

### Creating a Reference
In Python, references are created using the `id()` function. This function returns a unique identifier for an object, which can be used to create a reference to that object.

### Passing a Reference
Once a reference has been created, it can be passed as an argument to a function. The function can then access the object using the reference.

### Example
For example, suppose we have an object `x` and we want to pass it by reference to a function `f`. We can do this as follows:

```python
x_ref = id(x)
f(x_ref)
```

The function `f` can then access the object `x` using the reference `x_ref`.

### Modifying the Object
When a reference is passed to a function, the function can modify the object using the reference. For example, the following code will modify the object `x`:

```python
def f(x_ref):
    x = get_object_from_id(x_ref)
    x.some_attribute = some_value
```
