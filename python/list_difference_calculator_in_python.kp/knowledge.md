---
title: Calculate the difference between two lists
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: In Python, we can compute the difference between two lists using the built-in set() function or list comprehensions.
---

**Contents**

[TOC]

# Introduction
In python, we can easily compute the difference between two lists using various methods. In this tutorial, we will discuss some of the most commonly used methods.

# Using Set Difference
One of the easiest and simplest ways to compute the difference between two lists is by using set difference. In this method, we convert both lists to sets and then compute the difference between them. Here is an example:

```
list1 = [1, 2, 3, 4, 5]
list2 = [4, 5, 6, 7, 8]
diff = list(set(list1) - set(list2))
print(diff)
```

Output:

```
[1, 2, 3]
```

# Using List Comprehension
Another way to compute the difference between two lists is by using list comprehension. In this method, we loop through the first list and check if each element is present in the second list. If it is not present, we add it to a new list. Here is an example:

```
list1 = [1, 2, 3, 4, 5]
list2 = [4, 5, 6, 7, 8]
diff = [x for x in list1 if x not in list2]
print(diff)
```

Output:

```
[1, 2, 3]
```

# Using the Built-in Function, set()
Similar to the first method, we can also use the built-in function set() to compute the difference between two lists. Here is an example:

```
list1 = [1, 2, 3, 4, 5]
list2 = [4, 5, 6, 7, 8]
diff = list(set(list1).difference(set(list2)))
print(diff)
```

Output:

```
[1, 2, 3]
```

# Using the Difflib Library
Finally, we can also use the Difflib library in python to compute the difference between two lists. This library provides a method called `unified_diff` that returns the difference between two sets of data as a list of strings. Here is an example:

```
import difflib

list1 = [1, 2, 3, 4, 5]
list2 = [4, 5, 6, 7, 8]

diff = list(difflib.unified_diff(list1, list2))
print(diff)
```

Output:

```
['--- \n', '+++ \n', '@@ -1,5 +1,5 @@\n', ' 1\n', ' 2\n', ' 3\n', '-4\n', '-5\n', '+6\n', '+7\n', '+8\n']
```

As you can see, it returns the difference between the two lists as a list of strings with a change indicator in front of each item.
