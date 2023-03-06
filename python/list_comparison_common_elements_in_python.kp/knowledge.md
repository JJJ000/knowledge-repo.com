---
title: Comparison of the shared elements in two lists
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Using set() method to convert the lists into sets, and then using intersection() method on the sets will give the common elements between the 2 lists in Python.
---

**Contents**

[TOC]

## Introduction
When working with data, it's common to come across two or more lists with common elements that need to be compared. Python offers several ways to compare common elements between two lists, and the best approach depends on the situation.

## Using Sets
One of the easiest ways to compare common elements between two lists is to convert them into sets and then use the intersection() method to find the common items. This method returns a new set with only the elements that exist in both sets.

```python
list1 = [1, 2, 3, 4, 5]
list2 = [4, 5, 6, 7, 8]

set1 = set(list1)
set2 = set(list2)

common_elements = set1.intersection(set2)

print(common_elements)
```

Output:
```
{4, 5}
```

## Using list comprehension
Another way to compare common elements between two lists is to use list comprehension. This method involves iterating over one list and checking if its elements exist in the other list using the `in` keyword.

```python
list1 = [1, 2, 3, 4, 5]
list2 = [4, 5, 6, 7, 8]

common_elements = [element for element in list1 if element in list2]

print(common_elements)
```

Output:
```
[4, 5]
```

## Using a for loop
A third way to compare common elements between two lists involves using a for loop. This approach is similar to list comprehension, but it involves manually iterating over one list and checking if its elements exist in the other list.

```python
list1 = [1, 2, 3, 4, 5]
list2 = [4, 5, 6, 7, 8]

common_elements = []

for element in list1:
    if element in list2:
        common_elements.append(element)

print(common_elements)
```

Output:
```
[4, 5]
```

## Conclusion
Python offers several ways to compare common elements between two lists. The choice of approach depends on the situation, but some popular methods include using sets, list comprehension, and for loops.
