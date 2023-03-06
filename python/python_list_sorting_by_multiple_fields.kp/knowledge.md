---
title: Reorganizing a Python list based on two criteria
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: You can use the sorted() function with two lambda functions as arguments, each defining the sorting key for each field.
---

**Contents**

[TOC]

## Sorting by one field

The easiest way to sort a Python list by one field is to use the `sorted()` function. The `sorted()` function can take an optional `key` parameter, which is a function that takes each item in the list and returns a value that will be used for sorting.

For example, let's say we have a list of dictionaries representing people with their names and ages:

```python
people = [
    {'name': 'Alice', 'age': 25},
    {'name': 'Bob', 'age': 30},
    {'name': 'Charlie', 'age': 20},
]
```

We can sort this list by age using the `sorted()` function like this:

```python
sorted_people = sorted(people, key=lambda p: p['age'])
```

The `key` function we pass to `sorted()` is a lambda function that takes each dictionary `p` and returns its `'age'` value.

## Sorting by two fields

To sort a Python list by two fields, we can use the same technique as above, but pass a tuple of `key` functions to the `sorted()` function.

For example, let's say we want to sort the `people` list from above first by age, and then by name in alphabetical order. We can do this like so:

```python
sorted_people = sorted(people, key=lambda p: (p['age'], p['name']))
```

In this case, the `key` function we pass to `sorted()` is a lambda function that takes each dictionary `p` and returns a tuple of its `'age'` value and `'name'` value.

By default, Python sorts tuples in ascending order by each element, so this will first sort the list by age, and then by name within each age group.

## Sorting in reverse order

To sort a list in reverse order, we can pass the `reverse=True` argument to `sorted()`:

```python
sorted_people = sorted(people, key=lambda p: (p['age'], p['name']), reverse=True)
```

This will sort the list in descending order by age (i.e., oldest people first), and then in reverse alphabetical order by name within each age group.
