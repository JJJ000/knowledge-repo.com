---
title: Organizing the columns in a pandas dataframe according to the column label
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Pandas dataframes can be sorted by column name using the sort\_values() method.
---

**Contents**

[TOC]

**Section 1: Using the sort_values() Method**

The `sort_values()` method is the most straightforward way to sort a pandas dataframe based on a specific column name. This method takes two parameters, `by` and `ascending`, and returns a new sorted dataframe. The `by` parameter is used to specify the column name to sort by, while the `ascending` parameter is used to specify whether the sort should be in ascending (True) or descending (False) order.

For example, to sort a dataframe `df` by the column name `Name`, in descending order, we would use the following code:

```
df.sort_values(by='Name', ascending=False)
```

**Section 2: Using the sort_index() Method**

Another way to sort a pandas dataframe based on a specific column name is to use the `sort_index()` method. This method takes one parameter, `by`, and returns a new sorted dataframe. The `by` parameter is used to specify the column name to sort by.

For example, to sort a dataframe `df` by the column name `Name`, we would use the following code:

```
df.sort_index(by='Name')
```

**Section 3: Using the sort() Method**

The `sort()` method is yet another way to sort a pandas dataframe based on a specific column name. This method takes two parameters, `by` and `ascending`, and returns a new sorted dataframe. The `by` parameter is used to specify the column name to sort by, while the `ascending` parameter is used to specify whether the sort should be in ascending (True) or descending (False) order.

For example, to sort a dataframe `df` by the column name `Name`, in ascending order, we would use the following code:

```
df.sort(by='Name', ascending=True)
```

**Section 4: Using the sort_values() Method with Multiple Columns**

The `sort_values()` method can also be used to sort a pandas dataframe based on multiple column names. This method takes two parameters, `by` and `ascending`, and returns a new sorted dataframe. The `by` parameter is used to specify the list of column names to sort by, while the `ascending` parameter is used to specify whether the sort should be in ascending (True) or descending (False) order.

For example, to sort a dataframe `df` by the columns `Name` and `Age`, in descending order, we would use the following code:

```
df.sort_values(by=['Name', 'Age'], ascending=False)
```
