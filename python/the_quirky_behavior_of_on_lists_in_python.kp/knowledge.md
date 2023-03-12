---
title: What causes the unexpected behavior of += on lists?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: The += operator extends the existing list rather than creating a new one, which can lead to unexpected results when mutable objects like lists are involved.
---

**Contents**

[TOC]

## Introduction 

The Python language offers the `+=` operator to append a new element to a list. However, sometimes this operator does not behave as expected. In this answer, we will explore some of the reasons why the `+=` operator might behave unexpectedly on lists in Python, and we will provide solutions to prevent these issues.


## Mutable vs Immutable Types

Python types are divided into two categories: mutable and immutable. Immutable types, like integers or strings, cannot be modified once they are created. In contrast, mutable types like lists or dictionaries can be modified by adding, removing, or changing elements. 

When we use the `+=` operator with a mutable type, we are modifying the object in place. Essentially, we are appending new elements directly to the same list object. On the other hand, when we use the `+=` operator with an immutable type, Python creates a new object and assigns it to the variable. Therefore, the behavior of `+=` depends on the mutability of the variable.

```python
x = [1, 2, 3]
y = 4

# += on mutable type
x += [y]  # [1, 2, 3, 4]
print(x)

# += on immutable type
y += 1  # 5
print(y)
```

## List Concatenation

To avoid unexpected behavior when using the `+=` operator with a list, we can use the concatenation operator `+`. The `+` operator creates a new list object and appends the elements of the original lists. This operation never modifies the original lists, and it always returns a new object.

```python
x = [1, 2, 3]
y = 4

# list concatenation instead of +=
x = x + [y]  # [1, 2, 3, 4]
print(x)
```

## Using the Append Method

Another way to prevent unexpected behavior when appending to a list is to use the `append()` method. The `append()` method adds a new element to the end of the list, modifying it in place. This is a more explicit way of appending elements than using the `+=` operator because it does not rely on the operator's behavior.

```python
x = [1, 2, 3]
y = 4

# use the append method instead
x.append(y)  # [1, 2, 3, 4]
print(x)
```

## Conclusion

In conclusion, the `+=` operator in Python can behave unexpectedly on lists because it modifies the object in place. To prevent this behavior, we can use the concatenation operator `+` or the `append()` method to append new elements explicitly. Always keep in mind the mutability of Python types when using operators and methods that modify objects in place.
