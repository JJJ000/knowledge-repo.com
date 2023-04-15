---
title: Removing several items from a list
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Use a list comprehension or the filter() function with a lambda function to exclude the elements you want to delete.
---

**Contents**

[TOC]

Section 1: Introduction

Python provides an in-built method called `del()` which can be used to delete elements from a list. However, if you want to delete multiple elements from a list there are different approaches in Python you can use. In this guide, we will discuss some of the popular ways to delete multiple elements from a list in Python.

Section 2: Deleting Multiple Elements using a loop

One of the most straightforward ways to delete multiple elements from a list is by using a loop. Here is an example:

```
fruits = ["apple", "banana", "cherry", "orange", "kiwi", "mango"]
to_remove = [1, 3, 5]

for index in sorted(to_remove, reverse=True):
    del fruits[index]

print(fruits)
```
In this example, we create a list of fruits and another list named `to_remove` containing the indices of the elements we want to remove. We then iterate over the `to_remove` list in reverse order using the `sorted()` function with `reverse=True`, and use `del` to remove each element by index. Finally, we print the updated list of fruits.

Section 3: Deleting Multiple Elements using list comprehension

Another way to delete multiple elements from a list in Python is using list comprehension. Here is an example:

```
fruits = ["apple", "banana", "cherry", "orange", "kiwi", "mango"]
to_remove = [1, 3, 5]

fruits = [fruit for index, fruit in enumerate(fruits) if index not in to_remove]

print(fruits)
```

In the above example, we use list comprehension to create a new list of fruits where each fruit is selected only if its index is not in the `to_remove` list. Finally, we print the updated list of fruits.

Section 4: Conclusion

In this guide, we discussed two simple ways to delete multiple elements from a list in Python. You can use a loop to iterate over the indices of the elements to be removed, or use list comprehension to create a new list containing only the elements you want to keep. Depending on the size of the list, you can choose the best approach for your needs.
