---
title: Substitute the elements within the list with Python programming
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To replace values in a list using Python, you can iterate through the list and use indexing and assignment to replace the values.
---

**Contents**

[TOC]

## Creating a List

First, let's create a list with some initial values:

```python
my_list = [1, 2, 3, 4, 5]
```

This list contains the values `[1, 2, 3, 4, 5]`.

## Replacing Values

To replace a value in the list, we can access it using its index and assign a new value to it. For example, let's replace the second value (`2`) with `6`:

```python
my_list[1] = 6
```

This will change the list to `[1, 6, 3, 4, 5]`.

We can also replace multiple values at once by assigning a new list to a slice of the original list. For instance, let's replace the second and third values (`6` and `3`) with `7` and `8`:

```python
my_list[1:3] = [7, 8]
```

Now the list becomes `[1, 7, 8, 4, 5]`.

## Using Loops

To replace multiple values in the list conditionally or iteratively, we can use a loop. For example, let's replace all the even numbers in the list with `0`:

```python
for i in range(len(my_list)):
  if my_list[i] % 2 == 0:
    my_list[i] = 0
```

This will change the list to `[1, 0, 8, 0, 5]`.

We can also use list comprehension to achieve the same result in a more concise way:

```python
my_list = [0 if x % 2 == 0 else x for x in my_list]
```

This creates a new list with the same length and replaces each even value with `0`, resulting in `[1, 0, 8, 0, 5]`.
