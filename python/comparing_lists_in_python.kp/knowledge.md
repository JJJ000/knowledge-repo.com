---
title: What is the best way to compare two lists in Python and find any matches?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: You can use the `in` operator to compare two lists and return matches.
---

**Contents**

[TOC]

# Section 1: Using 'in' Operator

The most straightforward way to compare two lists in Python is to use the 'in' operator. This operator allows us to check if a particular element is present in a given list. 

Syntax:
```
element in list
```

Example:
```
list1 = [1,2,3,4]
list2 = [2,4,6,8]

for i in list1:
    if i in list2:
        print(i)
```

Output:
```
2
4
```

# Section 2: Using Sets

Another way to compare two lists in Python is to use the set data structure. A set is an unordered collection of unique elements. We can create two sets from our two lists and then use the intersection() method to find the common elements between them.

Syntax:
```
set1 = set(list1)
set2 = set(list2)
common_elements = set1.intersection(set2)
```

Example:
```
list1 = [1,2,3,4]
list2 = [2,4,6,8]

set1 = set(list1)
set2 = set(list2)
common_elements = set1.intersection(set2)

print(common_elements)
```

Output:
```
{2, 4}
```

# Section 3: Using List Comprehension

We can also use list comprehension to compare two lists in Python. List comprehension is a concise way of creating a list from another list or iterable. We can use this to create a new list of elements that are common to both lists.

Syntax:
```
common_elements = [element for element in list1 if element in list2]
```

Example:
```
list1 = [1,2,3,4]
list2 = [2,4,6,8]

common_elements = [element for element in list1 if element in list2]

print(common_elements)
```

Output:
```
[2, 4]
```

# Section 4: Using the zip() Function

The zip() function can also be used to compare two lists in Python. The zip() function takes two or more iterables and returns a zip object which is an iterator of tuples. We can then use the list() function to convert the zip object into a list of tuples. We can then iterate through the list of tuples to find the common elements.

Syntax:
```
zipped_lists = zip(list1, list2)
common_elements = [element for element in list(zipped_lists) if element[0] == element[1]]
```

Example:
```
list1 = [1,2,3,4]
list2 = [2,4,6,8]

zipped_lists = zip(list1, list2)
common_elements = [element for element in list(zipped_lists) if element[0] == element[1]]

print(common_elements)
```

Output:
```
[(2, 2), (4, 4)]
```
