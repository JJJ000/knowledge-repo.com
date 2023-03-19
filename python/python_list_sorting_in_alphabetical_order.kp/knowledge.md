---
title: Arrange a Python list of data structures in alphabetical order
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use the sort() method in Python to sort a list alphabetically.
---

**Contents**

[TOC]

## Sorting a list using the sort() method

The easiest way to sort a list alphabetically is by using the sort() method. This method modifies the list in place, meaning that it does not return anything but instead sorts the elements of the list directly.

```python
fruits = ["apple", "banana", "cherry", "kiwi", "orange"]
fruits.sort()
print(fruits)
```

Output:
```
['apple', 'banana', 'cherry', 'kiwi', 'orange']
```

## Sorting a list using the sorted() function

If you do not want to modify the original list and instead create a new sorted list, you can use the sorted() function. This function takes an iterable as an argument and returns a new list with the sorted elements.

```python
fruits = ["apple", "banana", "cherry", "kiwi", "orange"]
sorted_fruits = sorted(fruits)
print(sorted_fruits)
```

Output:
```
['apple', 'banana', 'cherry', 'kiwi', 'orange']
```

## Sorting a list in reverse alphabetical order

To sort a list in reverse alphabetical order, you can use the reverse parameter of either the sort() method or the sorted() function. This parameter takes a boolean value, where True means sorting in reverse order and False (or not specifying the parameter at all) means sorting in ascending order.

```python
fruits = ["apple", "banana", "cherry", "kiwi", "orange"]
fruits.sort(reverse=True)
print(fruits)

sorted_fruits = sorted(fruits, reverse=True)
print(sorted_fruits)
```

Output:
```
['orange', 'kiwi', 'cherry', 'banana', 'apple']
['orange', 'kiwi', 'cherry', 'banana', 'apple']
```

## Sorting a list of tuples by the second element in each tuple

If you have a list of tuples and want to sort them based on the second element of each tuple, you can pass a lambda function as the key parameter of the sort() method or sorted() function. This lambda function should return the second element of the tuple, which can be accessed using tuple indexing (`[1]`).

```python
fruits = [("apple", 3), ("banana", 2), ("cherry", 4), ("kiwi", 1), ("orange", 5)]
fruits.sort(key=lambda x: x[1])
print(fruits)

sorted_fruits = sorted(fruits, key=lambda x: x[1])
print(sorted_fruits)
```

Output:
```
[('kiwi', 1), ('banana', 2), ('apple', 3), ('cherry', 4), ('orange', 5)]
[('kiwi', 1), ('banana', 2), ('apple', 3), ('cherry', 4), ('orange', 5)]
```
