---
title: Arranging a collection of values in order
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: You can use the sorted() function in Python to sort a set of values in ascending order.
---

**Contents**

[TOC]

## Introduction 

There are several ways to sort a set of values in Python depending on the use case. In this article, we will explore various ways to sort a set of values in Python.

## Using sorted()

The built-in `sorted()` function in Python sorts the items in an iterable and returns a new sorted list. The original iterable is not modified. Here's an example:

``` python
numbers = [5, 2, 7, 1, 8]
sorted_numbers = sorted(numbers)
print(sorted_numbers)  # Output: [1, 2, 5, 7, 8]
```

In the above example, we have a list of numbers that we want to sort. We use the `sorted()` function to create a new `sorted_numbers` list with the sorted values.

## Using .sort()

The list method `.sort()` sorts the elements of a list in place, meaning that the original list is modified. It does not return a new list. Here's an example:

``` python
numbers = [5, 2, 7, 1, 8]
numbers.sort()
print(numbers)  # Output: [1, 2, 5, 7, 8]
```

In the above example, we use the `.sort()` method to modify the `numbers` list in place and sort it.

## Using lambda function and sorted()

We can also specify a lambda function to be used as the key for sorting the values using the `sorted()` function. Here's an example:

``` python
fruits = [('apple', 20), ('banana', 5), ('orange', 12), ('mango', 8)]
sorted_fruits = sorted(fruits, key=lambda x: x[1])
print(sorted_fruits)  # Output: [('banana', 5), ('mango', 8), ('orange', 12), ('apple', 20)]
```

In the above example, we have a list of tuples where the first element is the fruit name and the second element is the quantity. We use a lambda function to specify that we want to sort the list based on the second element of each tuple. The `sorted()` function then returns a new sorted list based on this criteria.

## Using operator module and sorted()

We can use the `operator` module to simplify the lambda function used as the key for sorting. Here's an example:

``` python
import operator

fruits = [('apple', 20), ('banana', 5), ('orange', 12), ('mango', 8)]
sorted_fruits = sorted(fruits, key=operator.itemgetter(1))
print(sorted_fruits)  # Output: [('banana', 5), ('mango', 8), ('orange', 12), ('apple', 20)]
```

In the above example, we use the `itemgetter()` function from the `operator` module to specify that we want to sort the list based on the second element of each tuple. The `sorted()` function then returns a new sorted list based on this criteria.

## Conclusion

In conclusion, there are several ways to sort a set of values in Python, including using the built-in `sorted()` function, the list method `.sort()`, lambda functions with `sorted()`, and the `operator` module with `sorted()`. The choice of which method to use depends on the use case and personal preference.
