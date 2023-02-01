---
title: What is the procedure for determining the number of times a certain element appears in an ndarray?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the numpy.count\_nonzero() function to count the occurrence of a certain item in an ndarray.
---

**Contents**

[TOC]

## Using numpy.count_nonzero()

The numpy.count_nonzero() function can be used to count the occurrence of a certain item in an ndarray. This function takes an array and returns the number of non-zero elements in the array. 

For example, if we have an array `a` as follows:

```
a = np.array([1, 0, 1, 0, 0, 1, 0, 0, 1, 1])
```

We can use the `numpy.count_nonzero()` function to count the occurrence of the value 1 in the array:

```
np.count_nonzero(a == 1)
```

The result of this expression will be `5`, which is the number of times the value 1 appears in the array.

## Using numpy.where()

The numpy.where() function can also be used to count the occurrence of a certain item in an ndarray. This function takes a condition as an argument and returns the indices of the elements in the array that satisfy the condition. 

For example, if we have an array `a` as follows:

```
a = np.array([1, 0, 1, 0, 0, 1, 0, 0, 1, 1])
```

We can use the `numpy.where()` function to count the occurrence of the value 1 in the array:

```
np.where(a == 1)
```

The result of this expression will be `(array([0, 2, 5, 8, 9]),)`, which is the indices of the elements in the array that are equal to 1. The length of this array is 5, which is the number of times the value 1 appears in the array.

## Using Python's built-in count() method

The built-in count() method can also be used to count the occurrence of a certain item in an ndarray. This method takes an element as an argument and returns the number of times it appears in the array. 

For example, if we have an array `a` as follows:

```
a = np.array([1, 0, 1, 0, 0, 1, 0, 0, 1, 1])
```

We can use the `count()` method to count the occurrence of the value 1 in the array:

```
a.count(1)
```

The result of this expression will be `5`, which is the number of times the value 1 appears in the array.

## Using list comprehensions

List comprehensions can also be used to count the occurrence of a certain item in an ndarray. This method takes an array and returns the number of times a certain element appears in the array. 

For example, if we have an array `a` as follows:

```
a = np.array([1, 0, 1, 0, 0, 1, 0, 0, 1, 1])
```

We can use list comprehensions to count the occurrence of the value 1 in the array:

```
len([x for x in a if x == 1])
```

The result of this expression will be `5`, which is the number of times the value 1 appears in the array.
