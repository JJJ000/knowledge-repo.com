---
title: What is the best way to add multiple items to a list in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can append multiple values to a list in Python by using the `list.extend()` method.
---

**Contents**

[TOC]

##### Using the append() Method
The append() method is used to add a single item to the end of a list. To append multiple items to a list, use a for loop.

##### Syntax
```
list.append(item)
```

##### Example
```
list = [1, 2, 3]

# Append multiple items to the list
for item in [4, 5, 6]:
    list.append(item)

print(list)

# Output: [1, 2, 3, 4, 5, 6]
```

##### Using the extend() Method
The extend() method is used to add multiple items to the end of a list.

##### Syntax
```
list.extend(iterable)
```

##### Example
```
list = [1, 2, 3]

# Extend the list with multiple items
list.extend([4, 5, 6])

print(list)

# Output: [1, 2, 3, 4, 5, 6]
```
