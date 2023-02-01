---
title: What is the syntax for creating an array in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: In Python, an array can be declared using the `array` module.
---

**Contents**

[TOC]

**Creating an Array**

Python does not have built-in support for Arrays, but Python Lists can be used instead.

**Using a List**

A list is a collection of items in a particular order. To create a list, use square brackets and separate the items with commas.

Example:

```
my_list = [1, 2, 3, 4]
```

**Accessing an Item**

To access an item in a list, use the index of the item in the list. Python uses zero-based indexing, so the first item in the list has an index of 0.

Example:

```
my_list = [1, 2, 3, 4]

# Access the second item in the list
item = my_list[1]

# Print the item
print(item)
# Output: 2
```

**Adding Items**

To add items to a list, use the `append()` method. This will add the item to the end of the list.

Example:

```
my_list = [1, 2, 3, 4]

# Add the number 5 to the list
my_list.append(5)

# Print the list
print(my_list)
# Output: [1, 2, 3, 4, 5]
```
