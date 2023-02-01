---
title: Take out all instances of a particular value from a list
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: list.remove(value)
---

**Contents**

[TOC]

**Section 1: Using a For Loop**

We can use a for loop to iterate through the list and remove all occurrences of a particular value.

```
my_list = [1, 2, 3, 4, 5, 5, 3]
value_to_remove = 3

for item in my_list:
    if item == value_to_remove:
        my_list.remove(item)

print(my_list) # [1, 2, 4, 5, 5]
```

**Section 2: Using a List Comprehension**

We can also use a list comprehension to remove all occurrences of a particular value.

```
my_list = [1, 2, 3, 4, 5, 5, 3]
value_to_remove = 3

my_list = [item for item in my_list if item != value_to_remove]

print(my_list) # [1, 2, 4, 5, 5]
```

**Section 3: Using filter()**

We can also use the built-in `filter()` function to remove all occurrences of a particular value.

```
my_list = [1, 2, 3, 4, 5, 5, 3]
value_to_remove = 3

my_list = list(filter(lambda x: x != value_to_remove, my_list))

print(my_list) # [1, 2, 4, 5, 5]
```

**Section 4: Using remove()**

We can also use the built-in `remove()` function to remove all occurrences of a particular value.

```
my_list = [1, 2, 3, 4, 5, 5, 3]
value_to_remove = 3

for item in my_list:
    my_list.remove(value_to_remove)

print(my_list) # [1, 2, 4, 5, 5]
```
