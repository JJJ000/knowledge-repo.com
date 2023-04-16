---
title: What is the procedure for removing an item from a list if it is present?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the remove() method to delete an item from a list if it exists.
---

**Contents**

[TOC]

#1 Using the `remove()` Method

The `remove()` method can be used to delete an item from a list if it exists.

Syntax:
```
list.remove(element)
```

Example:
```
fruits = ["apple", "banana", "cherry"]
fruits.remove("banana")
print(fruits)
```

Output:
```
['apple', 'cherry']
```

#2 Using the `del` Statement

The `del` statement can also be used to delete an item from a list if it exists.

Syntax:
```
del list[index]
```

Example:
```
fruits = ["apple", "banana", "cherry"]
del fruits[1]
print(fruits)
```

Output:
```
['apple', 'cherry']
```

#3 Using the `pop()` Method

The `pop()` method can be used to delete an item from a list if it exists.

Syntax:
```
list.pop(index)
```

Example:
```
fruits = ["apple", "banana", "cherry"]
fruits.pop(1)
print(fruits)
```

Output:
```
['apple', 'cherry']
```

#4 Using the `clear()` Method

The `clear()` method can be used to delete all items from a list.

Syntax:
```
list.clear()
```

Example:
```
fruits = ["apple", "banana", "cherry"]
fruits.clear()
print(fruits)
```

Output:
```
[]
```
