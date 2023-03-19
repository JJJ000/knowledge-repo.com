---
title: Rearranging the keys of a dictionary in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-14 00:00:00
updated_at: 2023-03-14 00:00:00
tldr: You can sort dictionary keys in Python using the sorted() function or by converting it into a list and then sorting it.
---

**Contents**

[TOC]

## Introduction

Dictionary keys in Python can be sorted in various ways, depending on the requirements of your program. Sorting the keys can help in accessing the values in a specific order, iterating through the keys in a certain order, or printing the dictionary in a specific sequence. In this article, we will discuss different methods to sort dictionary keys in Python.

## Method 1: Sorting using the sorted() function

The simplest way to sort a dictionary's keys is by using the built-in `sorted()` function. It returns an iterable in sorted order. Here is an example:

```
# Define a dictionary
my_dict = {'banana': 3, 'apple': 2, 'orange': 4}

# Get the sorted list of keys
sorted_keys = sorted(my_dict)

# Print the keys
print(sorted_keys)
```

Output:
```
['apple', 'banana', 'orange']
```

## Method 2: Sorting using the keys() method

Another way to sort dictionary keys is by using the `keys()` method of the dictionary, which returns a view object that represents the keys. You can convert this view object to a list and sort it using the built-in `sorted()` function. Here is an example:

```
# Define a dictionary
my_dict = {'banana': 3, 'apple': 2, 'orange': 4}

# Create a list of sorted keys
sorted_keys = sorted(my_dict.keys())

# Print the sorted keys
print(sorted_keys)
```

Output:
```
['apple', 'banana', 'orange']
```

## Method 3: Sorting in descending order

If you want to sort the keys in descending order, you can use the `reverse=True` parameter of the `sorted()` function. Here is an example:

```
# Define a dictionary
my_dict = {'banana': 3, 'apple': 2, 'orange': 4}

# Create a list of sorted keys in descending order
sorted_keys = sorted(my_dict, reverse=True)

# Print the sorted keys
print(sorted_keys)
```

Output:
```
['orange', 'banana', 'apple']
```

## Method 4: Sorting by values

Sometimes, you may want to sort the keys based on the values associated with them. For this, you can use the `sorted()` function and pass a lambda function as the `key` parameter, which returns the value associated with each key. Here is an example:

```
# Define a dictionary
my_dict = {'banana': 3, 'apple': 2, 'orange': 4}

# Create a list of sorted keys based on values
sorted_keys = sorted(my_dict, key=lambda x: my_dict[x])

# Print the sorted keys
print(sorted_keys)
```

Output:
```
['apple', 'banana', 'orange']
```

In the above example, we passed a lambda function that takes each key `x` and returns its corresponding value from the dictionary `my_dict[x]`. This lambda function is used as the `key` parameter for the `sorted()` function, which sorts the keys based on their values.
