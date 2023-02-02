---
title: What is the syntax for declaring and populating an array in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: To declare and add items to an array in Python, use the syntax `array\_name = [item1, item2, ...]`.
---

**Contents**

[TOC]

### Declaring an Array

Python does not have a built-in array data structure. Instead, it has a list data structure which is more versatile and can be used as an array. To declare an array, simply assign a list of elements to a variable.

```python
my_array = [1, 2, 3, 4]
```

### Adding Items to an Array

To add an item to the end of an array, use the `append()` method.

```python
my_array.append(5)
```

To add an item at a specific index, use the `insert()` method.

```python
my_array.insert(2, 10)
```

This will insert the value 10 at index 2, shifting the other elements to the right.

### Concatenating Arrays

To add multiple items to the end of an array, use the `extend()` method.

```python
my_array.extend([6, 7, 8])
```

This will add the elements 6, 7, and 8 to the end of `my_array`.
