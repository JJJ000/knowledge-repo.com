---
title: What is the definition of a two-dimensional array?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: A two-dimensional array in Python can be defined as a list of lists.
---

**Contents**

[TOC]

# Section 1: What is a Two-Dimensional Array?
A two-dimensional array is an array of arrays, where each array is a row in the two-dimensional array. It is a data structure that stores elements in a tabular form, consisting of rows and columns. 

# Section 2: Creating a Two-Dimensional Array
In Python, a two-dimensional array can be created with the following syntax:

```
array_name = [[element1, element2, ...],
              [element3, element4, ...],
              ...]
```

The elements in the array can be of any data type, including strings, integers, floats, and booleans.

# Section 3: Accessing Elements in a Two-Dimensional Array
To access an element in a two-dimensional array, you must provide two indices. The first index is the row number and the second index is the column number. For example, if you have a two-dimensional array named my_array, you can access the element at row 2 and column 3 with the following syntax:

```
my_array[2][3]
```

# Section 4: Modifying Elements in a Two-Dimensional Array
To modify an element in a two-dimensional array, you must provide two indices, the same as when accessing the element. For example, if you want to modify the element at row 2 and column 3 in the array my_array, you can use the following syntax:

```
my_array[2][3] = new_value
```

Where new_value is the new value you want to assign to the element.
