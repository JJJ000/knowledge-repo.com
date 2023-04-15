---
title: What is an effective way to compare two lists that are not ordered (not sets)?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Convert both lists to sets and compare them using the == operator.
---

**Contents**

[TOC]

## Convert lists to dictionaries

One efficient way to compare two unordered lists in Python is to convert each list into a dictionary. The dictionary key will be the item in the list, and the dictionary value will be the frequency count of that item in the list. Then, we can compare the two dictionaries to determine if they are equal. This method is faster than sorting the lists and comparing them, especially if the lists have a large size.

```python
list1 = [1, 2, 3, 4, 4, 5]
list2 = [5, 4, 3, 2, 1, 4]

# Convert lists to dictionaries
dict1 = {}
dict2 = {}

for item in list1:
    dict1[item] = dict1.get(item, 0) + 1

for item in list2:
    dict2[item] = dict2.get(item, 0) + 1

# Compare dictionaries
if dict1 == dict2:
    print("Lists are equal")
else:
    print("Lists are not equal")
```

Output:

```
Lists are equal
```

## Counter module

Another efficient way to compare two unordered lists in Python is to use the Counter module from the collections library. The Counter module is a dictionary subclass that counts the frequency of each element in a list.

```python
from collections import Counter

list1 = [1, 2, 3, 4, 4, 5]
list2 = [5, 4, 3, 2, 1, 4]

# Use Counter module to count the frequency of each element
count1 = Counter(list1)
count2 = Counter(list2)

# Compare Counter objects
if count1 == count2:
    print("Lists are equal")
else:
    print("Lists are not equal")
```

Output:

```
Lists are equal
```

## Convert lists to sets

We can also convert the lists to sets and compare them using the set equality operator. However, this method only works if there are no duplicates in the lists.

```python
list1 = [1, 2, 3, 4, 5]
list2 = [5, 4, 3, 2, 1]

# Convert lists to sets
set1 = set(list1)
set2 = set(list2)

# Compare sets
if set1 == set2:
    print("Lists are equal")
else:
    print("Lists are not equal")
```

Output:

```
Lists are equal
```

## Compare using set operations

If there are duplicates in the lists, we can still use the set operations to compare them. We can first create sets from the lists and then use the set intersection operator to find the common elements between the sets. If the length of the intersection is equal to the length of either set, then the lists are equal.

```python
list1 = [1, 2, 3, 4, 4, 5]
list2 = [5, 4, 3, 2, 1, 4]

# Convert lists to sets and find the common elements
set1 = set(list1)
set2 = set(list2)
common = set1 & set2

# Compare lengths of the sets
if len(common) == len(set1) == len(set2):
    print("Lists are equal")
else:
    print("Lists are not equal")
```

Output:

```
Lists are equal
```
