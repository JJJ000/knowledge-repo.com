---
title: Reorganize the index following the sorting of the data-frame
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the reset\_index() method in pandas to update the index after sorting a data-frame in Python.
---

**Contents**

[TOC]

# Sections:
## Introduction
## Sorting the data-frame
## Updating the index after sorting
## Conclusion


## Introduction
Indexing of data is an essential component of data analysis. It helps in accessing specific items of data for faster and more straightforward analysis. In Python, Pandas library provides the DataFrame structure that allows for data indexing. It also provides an efficient way to sort data in the DataFrame structure.


## Sorting the data-frame
Sorting is the process of arranging data in a particular order, usually ascending or descending. To sort a data-frame in a pandas library, we use the function `sort_values()`. The syntax of `sort_values()` function is as follows:
```python
DataFrame.sort_values(by, axis=0, ascending=True, 
                      inplace=False, kind='quicksort', 
                      na_position='last')
```
Here,

`by`: It takes a string as input, which is the name of the column along which the data-frame is sorted.

`axis`: It takes an integer as input, which signifies the axis along which the data-frame is sorted. It can be 0 or 1, representing the rows or columns, respectively.

`ascending`: It takes a Boolean value as input. If True, then the data-frame is sorted in ascending order. If False, the data-frame is sorted in descending order.

The `sort_values()` function can sort a data-frame based on a single column or multiple columns. Sorting in ascending or descending order is also possible. 


## Updating the index after sorting
The `sort_values()` function, by default, does not update the index values of the sorted data-frame. Therefore we need to use another function called `reset_index()`. The `reset_index()` function assigns new index values to the data-frame in ascending order. 

The syntax of `reset_index()` function is as follows:
```python
   DataFrame.reset_index(level=None, drop=False, 
                          inplace=False, col_level=0, 
                          col_fill='')
```
Here,

`level`: It takes an integer or a label as input, which signifies the level or column of the data-frame to reset the index. 

`drop`: It takes a Boolean value as input. If True, then the old index is removed, and the new index is assigned to the data-frame. If False, then the old index is retained, and a new index column is added to the data-frame.

`inplace`: It takes a Boolean value as input. If True, then the new index is assigned to the data-frame itself. If False, a new data-frame is returned with the new index.

`col_level`: It takes an integer or a label as input, which signifies the level or column of the data-frame for which the index will be reset.

`col_fill`: It takes a value as input, which is used to fill missing values in the index.

The `reset_index()` function also has parameters to reset MultiIndex, which is beyond this scope of our topic.


## Conclusion
Sorting the data-frame is an essential task for data analysis. In Python, the pandas library provides the `sort_values()` function to sort a data-frame. However, after sorting the data-frame, we need to update the index values to reflect the actual order, which can be achieved by using the `reset_index()` function.
