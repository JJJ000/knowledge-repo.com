---
title: What are the differences between pandas' loc, iloc, at, and iat functions?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: loc label-based indexing, iloc integer-based indexing, at label-based scalar access, and iat integer-based scalar access are four methods to access and manipulate data in pandas dataframes and series in Python.
---

**Contents**

[TOC]

# Introduction to Pandas loc, iloc, at and iat

Pandas is an open-source data manipulation tool in Python that provides in-built data structures, high-level data analysis, and manipulation tools. As a data analyst, you will often find yourself working with data in various formats, in Python Pandas, this task is performed using its data manipulation functions such as `loc`, `iloc`, `at`, and `iat`.

# loc vs iloc

The `loc` and `iloc` are used to select data based on specific value(s) or label(s). Here is the difference between the two:

### loc
`loc` is short for `locate` which is used to refer the rows by their labels. It accepts label-based indexing i.e., the name of the index, row-label, or column-label.

Syntax: 

```python
df.loc[row_label,column_label]
```

### iloc 
`iloc` is short for `integer locate` which is used to refer to the rows or columns by their integer position. It only accepts the integer arguments.

Syntax:

```python
df.iloc[row_index,column_index]
```

# at vs iat

Both `at` and `iat` are used to access the scalar values at certain location or position of the DataFrame, the difference between the two is that `at` uses the index labels to access the location, while `iat` uses the integer location of the DataFrame.

### at

Syntax:

```python
df.at[row_label, column_label] = new_value
```

### iat

Syntax:

```python
df.iat[row_index, column_index] = new_value
```

# Conclusion

These four indexing functions in pandas have their own unique purpose and can be used interchangeably based on the requirement of the project.
