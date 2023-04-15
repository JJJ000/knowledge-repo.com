---
title: What is the method for removing the last item from a list?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: To delete the last item in a list in Python, use the pop() method with the index value of -1.
---

**Contents**

[TOC]

## Using the pop() method

One simple approach to removing the last item from a list in Python is to use the built-in `pop()` method. This method removes and returns the last item in the list, which makes it a convenient way to delete the last element without having to refer to its index directly.

```python
my_list = [1, 2, 3, 4, 5]  # original list
my_list.pop()  # remove the last item
print(my_list)  # [1, 2, 3, 4]
```

In this example, the `pop()` method is called on the list `my_list` to remove its last item (which is `5`). The list is then printed to show that the last item has been successfully deleted.

## Using slicing

Another way to delete the last item from a list is to use slicing. Unlike the `pop()` method, using slicing doesn't modify the original list; instead, it creates a new list that excludes the last item.

```python
my_list = [1, 2, 3, 4, 5]  # original list
new_list = my_list[:-1]  # create a new list without the last item
print(new_list)  # [1, 2, 3, 4]
```

In this example, the slicing notation `[:-1]` is used to create a new list that includes all the items in the original list except for the last one. The new list is then printed to show that it doesn't contain the last item (`5`).

## Modifying the list directly

If you don't need to keep the original list intact and want to modify it directly, you can also delete the last item by using the `del` statement with indexing.

```python
my_list = [1, 2, 3, 4, 5]  # original list
del my_list[-1]  # delete the last item of the list
print(my_list)  # [1, 2, 3, 4]
```

In this example, the `del` statement is used to delete the last item of the list by referring to its index (`-1`). The modified list is then printed to confirm that the last item has been deleted.
