---
title: What is the most efficient way to delete the first element from a list?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Use the del statement to remove the first item from a list in Python.
---

**Contents**

[TOC]

#Using pop()

##Description
The `pop()` method removes the item at the given index from the list and returns the removed item.

##Syntax
`list.pop(index)`

##Example
```
my_list = [1, 2, 3, 4]

# Remove the first item from the list
first_item = my_list.pop(0)

print(first_item) # Output: 1
print(my_list) # Output: [2, 3, 4]
```

#Using del

##Description
The `del` statement removes the item at the given index from the list.

##Syntax
`del list[index]`

##Example
```
my_list = [1, 2, 3, 4]

# Remove the first item from the list
del my_list[0]

print(my_list) # Output: [2, 3, 4]
```
