---
title: What is the process of verifying if all items from the following list are present?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: Check if all items are in the list using the built-in all() function.
---

**Contents**

[TOC]

# Introduction
In Python, it is possible to check if all the items in a list exist in another list. There are different ways to do this, and we will explore some of these methods in this tutorial. 

# Using 'all' Method
One way to check if all the items are in a list is to use the built-in 'all' function. The 'all' function returns True only if all the elements in the iterable are true.

```python
list = [1, 2, 3, 4, 5]
items_to_check = [1, 2, 3]

if all(i in list for i in items_to_check):
    print("All items are in the list")
else:
    print("There are missing items")
```

In this example, the 'all' function is used to iterate over the 'items_to_check' list and check if each element is in the 'list'. If all the elements are in the 'list', the message "All items are in the list" is printed; otherwise, the message "There are missing items" is printed.

# Using sets
Another way to check if all items are present in a list is to convert both lists to sets and check if the set of items to check is a subset of the set of the original list.

```python
list = [1, 2, 3, 4, 5]
items_to_check = [1, 2, 3]

if set(items_to_check).issubset(set(list)):
    print("All items are in the list")
else:
    print("There are missing items")
```

In this example, we use the `issubset` method to check whether the items of the on list are all in the other. If all the items are in the 'list', the message "All items are in the list" is printed; otherwise, the message "There are missing items" is printed.

# Using 'difference' Method
We can use the difference method to find if there are any missing items in the list. If there is no difference between the two lists, then all the elements are present.

```python
list = [1, 2, 3, 4, 5]
items_to_check = [1, 2, 3]

diff = set(items_to_check).difference(set(list))

if len(diff) == 0:
    print("All items are in the list")
else:
    print("There are missing items")
```

In this example, we use the 'difference' function to find the difference between the two sets. If there is no difference, then all the elements in 'items_to_check' are present in the 'list', and the message "All items are in the list" is printed; otherwise, the message "There are missing items" is printed.

# Conclusion
In this tutorial, we explored different methods of checking whether all the items exist in a Python list. We used the 'all' function, sets and difference functions to check if there are any missing items in the list. Each of these methods is effective in its way, and it's up to you to choose the one that best suits your needs.
