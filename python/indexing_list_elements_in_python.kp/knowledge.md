---
title: Retrieve multiple items from a list using their indices
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: You can access multiple elements of a list by using the list`s index numbers and slicing notation.
---

**Contents**

[TOC]

#### Using the List Index Method

The list index method allows us to access multiple elements of a list knowing their index. This can be done by providing the list and the index of the elements that we want to access, separated by commas. For example: 

```
my_list = [1, 2, 3, 4, 5]

element1 = my_list[0]
element2 = my_list[2]
element3 = my_list[4]

print(element1, element2, element3)
```

This will output `1 3 5`.

#### Using the List Slicing Method

The list slicing method allows us to access multiple elements of a list knowing their index. This can be done by providing the list and the index range of the elements that we want to access, separated by a colon. For example: 

```
my_list = [1, 2, 3, 4, 5]

elements = my_list[0:3]

print(elements)
```

This will output `[1, 2, 3]`.

#### Using the List Comprehension Method

The list comprehension method allows us to access multiple elements of a list knowing their index. This can be done by providing the list and the index of the elements that we want to access, separated by commas, inside a list comprehension. For example: 

```
my_list = [1, 2, 3, 4, 5]

elements = [my_list[0], my_list[2], my_list[4]]

print(elements)
```

This will output `[1, 3, 5]`.

#### Using the For Loop Method

The for loop method allows us to access multiple elements of a list knowing their index. This can be done by providing the list and looping through it, checking the index of each element. For example: 

```
my_list = [1, 2, 3, 4, 5]

elements = []

for i in range(len(my_list)):
    if i == 0 or i == 2 or i == 4:
        elements.append(my_list[i])

print(elements)
```

This will output `[1, 3, 5]`.
