---
title: Is it possible to reset iterators in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: No, iterators cannot be reset in Python, they need to be recreated.
---

**Contents**

[TOC]

## Overview of Iterators in Python

Iterators are a useful programming tool in Python that help in accessing the elements of a collection one at a time, without having to know the underlying implementation details. Iterator objects are created from iterable objects like lists, tuples or dictionaries. 

## Iterators in Python are Unidirectional

Iterators in Python are unidirectional which means that they can only iterate through an object in one direction. It means that once an iterator object reaches the end of an iterable object, it cannot go back to the beginning of the object to start over. 

## You cannot reset iterators in Python

In Python, iterators do not have any method or function to reset their position to the beginning of the iterable object. Thus it means that once an iterator reaches the end of the iterable object, or it has been exhausted, it cannot be reset to return to the start or any arbitrary position in the iterable object. 

## Workaround to Reset Iterators

However, a workaround can still be used to create a new iterator object from an iterable object by using the original object. For instance, one can use list() function to create a new list object and then use the iter() function to create an iterator object from the list object. This approach can be used to simulate resetting the iterator object to the beginning of the iterable object. 

```python
lst = [1,2,3,4,5]
it1 = iter(lst)  # create iterator 1 from a list
it2 = iter(list(lst))  # create iterator 2 by creating a new list and iterating from the start of the list
print(next(it1))  # print 1
print(next(it1))  # print 2
print(next(it2))  # print 1
``` 

In conclusion, although Python iterators are unidirectional and thus do not have any method to reset their position to the beginning of an iterable object, a workaround can be used to create a new iterator object from an iterable object. This approach can be used to simulate resetting the iterator object to the start of the iterable object.
