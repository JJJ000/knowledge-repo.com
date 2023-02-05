---
title: Use a pandas function to generate multiple new columns from a single column?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Pandas` `str.split` function can be used to create multiple new columns from a single column.
---

**Contents**

[TOC]

**Section 1: Create a New Column**

Pandas provides a variety of functions that can be used to create new columns. To create a new column, you can use the `assign()` function. This function takes a keyword argument, `columns`, which is a dictionary of column names and the values that should be assigned to each column.

For example, if you have a DataFrame with a column called `A` and you want to create a new column called `B` with the value `1`, you can use the following code:

```
df.assign(B=1)
```

**Section 2: Apply a Function to a Column**

Another common task is to apply a function to a column. You can do this using the `apply()` function. This function takes a function as its first argument and a column name as its second argument. 

For example, if you have a DataFrame with a column called `A` and you want to apply the `abs()` function to it, you can use the following code:

```
df['A'].apply(abs)
```

**Section 3: Create Multiple New Columns**

You can also use the `assign()` function to create multiple new columns at once. This can be done by passing a dictionary to the `columns` argument. The keys in the dictionary should be the names of the new columns and the values should be the values that should be assigned to each column.

For example, if you have a DataFrame with a column called `A` and you want to create two new columns called `B` and `C` with the values `1` and `2`, respectively, you can use the following code:

```
df.assign(B=1, C=2)
```

**Section 4: Apply Multiple Functions to a Column**

You can also apply multiple functions to a column using the `apply()` function. This can be done by passing a list of functions as the first argument. The second argument should be the name of the column. 

For example, if you have a DataFrame with a column called `A` and you want to apply the `abs()` and `round()` functions to it, you can use the following code:

```
df['A'].apply([abs, round])
```
