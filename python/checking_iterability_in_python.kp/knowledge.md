---
title: How can I tell if an object is iterable in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: You can determine if an object is iterable by using the built-in function `iter()` to test if the object is iterable.
---

**Contents**

[TOC]

## Checking for Iterability

Python provides a few ways to check if an object is iterable.

### Using the Iter Function

The built-in `iter()` function can be used to test if an object is iterable. If the object is iterable, `iter()` will return an iterator object. If the object is not iterable, `iter()` will raise a `TypeError` exception.

```python
# Sample iterable
iterable = [1, 2, 3]

# Check if iterable
iterator = iter(iterable)

# Print type
print(type(iterator))
```

Output:
```
<class 'list_iterator'>
```

### Using the isinstance Function

The `isinstance()` function can also be used to check if an object is iterable. The `isinstance()` function takes two arguments: the object to check and the type of the object. To check if an object is iterable, the second argument should be `collections.abc.Iterable`.

```python
# Sample iterable
iterable = [1, 2, 3]

# Check if iterable
is_iterable = isinstance(iterable, collections.abc.Iterable)

# Print result
print(is_iterable)
```

Output:
```
True
```

### Using the hasattr Function

The `hasattr()` function can also be used to check if an object is iterable. The `hasattr()` function takes two arguments: the object to check and the name of the attribute to check for. To check if an object is iterable, the second argument should be `__iter__`.

```python
# Sample iterable
iterable = [1, 2, 3]

# Check if iterable
has_iter = hasattr(iterable, '__iter__')

# Print result
print(has_iter)
```

Output:
```
True
```
