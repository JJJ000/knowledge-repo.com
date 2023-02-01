---
title: What is the process for determining if a column is present in a pandas dataframe?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: You can use the `in` keyword to check if a column exists in a Pandas DataFrame.
---

**Contents**

[TOC]

# Section 1: Using 'in' Operator

The simplest way to check if a column exists in Pandas is to use the 'in' operator. This is done by checking if the column name is present in the list of column names of the dataframe.

```
if column_name in df.columns:
    print('Column exists')
else:
    print('Column does not exist')
```

# Section 2: Using 'try/except' Block

Another way to check if a column exists in Pandas is to use a 'try/except' block. This is done by attempting to access the column and catching the exception if it does not exist.

```
try:
    df[column_name]
    print('Column exists')
except KeyError:
    print('Column does not exist')
```

# Section 3: Using 'hasattr' Function

The 'hasattr' function can also be used to check if a column exists in Pandas. This is done by checking if the dataframe has an attribute with the name of the column.

```
if hasattr(df, column_name):
    print('Column exists')
else:
    print('Column does not exist')
```

# Section 4: Using 'DataFrame.columns.contains' Method

The 'DataFrame.columns.contains' method can also be used to check if a column exists in Pandas. This is done by checking if the column is present in the list of column names of the dataframe.

```
if df.columns.contains(column_name):
    print('Column exists')
else:
    print('Column does not exist')
```
