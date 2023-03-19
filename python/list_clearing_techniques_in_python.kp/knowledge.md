---
title: Various methods of eliminating lists
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: There are multiple ways to clear lists in Python, including reassignment, using the clear() method, and using slice assignment to remove all elements.
---

**Contents**

[TOC]

# Using the clear() method

The clear() method is a built-in list method that removes all the elements from a list. Here is an example:

```
my_list = [1, 2, 3, 4, 5]
my_list.clear()
print(my_list)
```

Output:

```
[]
```

# Assigning an empty list to the existing list

Another way to clear a list is to assign an empty list to the existing list. Here is an example:

```
my_list = [1, 2, 3, 4, 5]
my_list = []
print(my_list)
```

Output:

```
[]
```

# Using slicing

Slicing is a way to get a subset of a list. We can also use slicing to remove all the elements from a list. Here is an example:

```
my_list = [1, 2, 3, 4, 5]
my_list[:] = []
print(my_list)
```

Output:

```
[]
```

# Using pop() method in a loop

We can also use a loop with the pop() method to remove all the elements from a list. Here is an example:

```
my_list = [1, 2, 3, 4, 5]
while my_list:
    my_list.pop()
print(my_list)
```

Output:

```
[]
```
