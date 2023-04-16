---
title: What is the best way to add an item to the beginning of a small Python list?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can prepend to a short Python list by using the `insert` method.
---

**Contents**

[TOC]

## Using the Insert Method
The insert method can be used to prepend elements to a list. This method takes two arguments, the index of the element to be inserted and the element itself. To prepend an element to a list, the index should be 0.

For example, to prepend the number 1 to the list `my_list`:

```python
my_list = [2, 3, 4]
my_list.insert(0, 1)
```

The list `my_list` will now be `[1, 2, 3, 4]`.

## Using the Plus Operator
The plus operator (`+`) can be used to combine two lists. To prepend an element to a list, the element should be added to a list containing the original list.

For example, to prepend the number 1 to the list `my_list`:

```python
my_list = [2, 3, 4]
my_list = [1] + my_list
```

The list `my_list` will now be `[1, 2, 3, 4]`.

## Using the Slice Assignment
The slice assignment can be used to prepend elements to a list. This method takes three arguments, the start index, the end index, and the element to be inserted. To prepend an element to a list, the start index should be 0 and the end index should be 0.

For example, to prepend the number 1 to the list `my_list`:

```python
my_list = [2, 3, 4]
my_list[0:0] = [1]
```

The list `my_list` will now be `[1, 2, 3, 4]`.
