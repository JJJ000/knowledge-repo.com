---
title: What are the solutions to resolve the typeerror unhashable type 'list'?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Convert the list to a tuple or use it as a value in a dictionary rather than as a key.
---

**Contents**

[TOC]

# Overview

In Python, we sometimes encounter the TypeError: unhashable type: 'list' error message. This error message usually occurs when we try to use a list as a key in a dictionary or as an element of a set. This error message means that the list is unhashable, which means it cannot be used as a key in a dictionary or as an element of a set. This error message can be frustrating, but there are ways to overcome it. In this article, we will discuss the common causes of this error message and several ways to fix it.

# Common Causes of TypeError: unhashable type: 'list'

Here are some common causes of the TypeError: unhashable type: 'list' error message:

1. Using a list as a key in a dictionary.
2. Using a list as an element of a set.
3. Using a list as an element of another data structure that requires hashable elements.

# How to Fix TypeError: unhashable type: 'list'

Here are three ways to fix the TypeError: unhashable type: 'list' error:

## 1. Convert the list to a tuple

One way to fix this error message is to convert the list to a tuple. In Python, tuples are hashable, which means they can be used as keys in a dictionary or as elements of a set. Here's an example:

```
my_list = [1, 2, 3]
my_dict = {(1, 2, 3): 'hello'}
```

In this example, we convert the list to a tuple and use it as a key in the dictionary.

## 2. Use a frozenset

Another way to fix this error message is to use a frozenset. A frozenset is an immutable set, which means it cannot be changed after it is created. In Python, frozensets are hashable, which means they can be used as keys in a dictionary or as elements of a set. Here's an example:

```
my_list = [1, 2, 3]
my_set = {frozenset(my_list): 'hello'}
```

In this example, we use a frozenset instead of a list as an element of a set.

## 3. Change the data structure

Finally, another way to fix this error message is to change the data structure. If we are using a data structure that requires hashable elements, we can switch to a data structure that does not require hashable elements. For example, we can switch from a dictionary to a list of tuples. Here's an example:

```
my_dict = {'person1': [1, 2, 3], 'person2': [4, 5, 6]}
my_list = [('person1', [1, 2, 3]), ('person2', [4, 5, 6])]
```

In this example, we switch from a dictionary to a list of tuples, which allows us to use lists as elements of the data structure.

# Conclusion

In conclusion, the TypeError: unhashable type: 'list' error message can be frustrating, but there are ways to overcome it. We can convert the list to a tuple, use a frozenset, or change the data structure. By understanding the causes of this error message and implementing one of these solutions, we can avoid this error message and write more effective Python code.
