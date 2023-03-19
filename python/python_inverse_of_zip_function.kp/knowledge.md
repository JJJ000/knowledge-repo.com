---
title: Can you provide the reverse function of zip in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: The inverse function of zip in Python is the unzip function, which separates a list of tuples into separate lists.
---

**Contents**

[TOC]

## The `zip` function in Python

The `zip` function is a built-in function in Python that takes two or more iterables and returns an iterator that aggregates the elements from each of the iterables. The resulting iterator yields tuples, each containing one element from each iterable. 

Here's an example of how the `zip` function works:

```
>>> list1 = [1, 2, 3]
>>> list2 = ['a', 'b', 'c']
>>> zipped = zip(list1, list2)
>>> list(zipped)
[(1, 'a'), (2, 'b'), (3, 'c')]
```

## The need for an inverse function for `zip`

While the `zip` function can be very useful in combining multiple lists, tuples, or other iterables, there may be cases where we need to separate these elements again. For example, consider the following code:

```
>>> names = ['Alice', 'Bob', 'Charlie']
>>> ages = [25, 32, 20]
>>> zipped = zip(names, ages)
>>> print(list(zipped))
[('Alice', 25), ('Bob', 32), ('Charlie', 20)]
```

Suppose we later want to extract the `names` and `ages` lists from the above zipped output. This is where we would need an inverse function for `zip`.

## The `unzip` function in Python

The inverse function for `zip` in Python is called `unzip`. However, unlike `zip`, there is no built-in function for `unzip`. 

One way to define an `unzip` function is as follows:

```
def unzip(zipped):
    lst1 = []
    lst2 = []
    for item in zipped:
        lst1.append(item[0])
        lst2.append(item[1])
    return lst1, lst2
```

Here's how we can use this `unzip` function to extract the `names` and `ages` lists from the example above:

```
>>> mylist = [('Alice', 25), ('Bob', 32), ('Charlie', 20)]
>>> names, ages = unzip(mylist)
>>> print(names)
['Alice', 'Bob', 'Charlie']
>>> print(ages)
[25, 32, 20]
```

## A more general `unzip` function using arguments

The `unzip` function defined above works specifically for zipped lists of two items each. However, we can define a more general `unzip` function that takes any number of zipped iterables as arguments and returns a tuple of lists, with one list for each original iterable.

Here's an example of how this more general `unzip` function might be defined:

```
def unzip(*zipped):
    return tuple([item[i] for item in zipped] for i in range(len(zipped)))

```

Here's how we can use this `unzip` function to extract the `names`, `ages`, and `genders` lists from the following example:

```
>>> names = ['Alice', 'Bob', 'Charlie']
>>> ages = [25, 32, 20]
>>> genders = ['F', 'M', 'M']
>>> zipped = zip(names, ages, genders)
>>> names_list, ages_list, genders_list = unzip(*zipped)
>>> print(names_list)
['Alice', 'Bob', 'Charlie']
>>> print(ages_list)
[25, 32, 20]
>>> print(genders_list)
['F', 'M', 'M']
```

Note that we use the `*` operator to unpack the zipped iterable into separate arguments for the `unzip` function.
