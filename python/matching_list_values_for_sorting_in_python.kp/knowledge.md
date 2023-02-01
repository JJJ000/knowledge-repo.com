---
title: Arranging the items of one list in accordance with the values of another list
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the sorted() function with the key parameter set to the values from the other list.
---

**Contents**

[TOC]

#### Section 1: Using zip() and sorted()

The `zip()` function takes two or more lists and creates a list of tuples, where the first item in each passed list is paired together, and so on. The `sorted()` function takes an iterable and returns a sorted list.

We can use `zip()` to pair the values from two lists, and then use `sorted()` to sort the list based on the values from one of the lists.

```python
list1 = [2, 5, 3, 4, 1]
list2 = ['a', 'b', 'c', 'd', 'e']

# Zip the two lists
zipped_lists = zip(list1, list2)

# Sort the zipped list
sorted_zipped_lists = sorted(zipped_lists)

# Unzip the zipped list
sorted_list1, sorted_list2 = zip(*sorted_zipped_lists)

print(sorted_list1)  # (1, 2, 3, 4, 5)
print(sorted_list2)  # ('e', 'a', 'c', 'd', 'b')
```

#### Section 2: Using lambda and sorted()

The `lambda` keyword is used to create anonymous functions, which can be used to pass a custom sorting function to the `sorted()` function.

We can use `lambda` to create a custom sorting function that takes two items from the list and compares them based on the values from the other list.

```python
list1 = [2, 5, 3, 4, 1]
list2 = ['a', 'b', 'c', 'd', 'e']

# Sort list1 based on the values in list2
sorted_list1 = sorted(list1, key=lambda x: list2[list1.index(x)])

print(sorted_list1)  # (1, 2, 3, 4, 5)
```

#### Section 3: Using operator.itemgetter() and sorted()

The `operator.itemgetter()` function takes a sequence of keys and returns a callable object that can be used to access the values from a dictionary.

We can use `operator.itemgetter()` to create a custom sorting function that takes two items from the list and compares them based on the values from the other list.

```python
list1 = [2, 5, 3, 4, 1]
list2 = ['a', 'b', 'c', 'd', 'e']

# Create a dictionary from the two lists
dict1 = dict(zip(list1, list2))

# Sort list1 based on the values in list2
sorted_list1 = sorted(list1, key=operator.itemgetter(*dict1))

print(sorted_list1)  # (1, 2, 3, 4, 5)
```

#### Section 4: Using sorted() and list comprehension

The `sorted()` function can also be used with a list comprehension to sort a list based on the values from another list.

We can use the `sorted()` function and a list comprehension to create a new list, sorted based on the values from the other list.

```python
list1 = [2, 5, 3, 4, 1]
list2 = ['a', 'b', 'c', 'd', 'e']

# Sort list1 based on the values in list2
sorted_list1 = sorted([x for x in list1], key=list2.index)

print(sorted_list1)  # (1, 2, 3, 4, 5)
```
