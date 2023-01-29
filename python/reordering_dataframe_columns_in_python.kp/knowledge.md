---
title: What is the process for rearranging the columns of a dataframe?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: You can change the order of DataFrame columns in Python by using the df.reindex() method.
---

**Contents**

[TOC]

### Method 1: Reordering Columns by Name

The simplest way to reorder the columns of a DataFrame is to use the `DataFrame.reindex` method. This method takes a list of column names as its argument, and returns a DataFrame with the columns in the order specified.

For example, if we have a DataFrame with columns A, B, and C, we can use `DataFrame.reindex` to reorder them as B, C, A:

```
df = df.reindex(columns=['B', 'C', 'A'])
```

### Method 2: Reordering Columns by Index

Another way to reorder the columns of a DataFrame is to use the `DataFrame.iloc` method. This method takes a list of column indices as its argument, and returns a DataFrame with the columns in the order specified.

For example, if we have a DataFrame with columns A, B, and C, we can use `DataFrame.iloc` to reorder them as B, C, A:

```
df = df.iloc[:, [1, 2, 0]]
```

### Method 3: Reordering Columns using Pandas

The `pandas` library provides a convenient way to reorder the columns of a DataFrame. The `DataFrame.reindex` method can be used to reorder the columns of a DataFrame by name, and the `DataFrame.iloc` method can be used to reorder the columns of a DataFrame by index.

### Method 4: Reordering Columns using Numpy

The `numpy` library provides a convenient way to reorder the columns of a DataFrame. The `np.rollaxis` method can be used to reorder the columns of a DataFrame by index, and the `np.argsort` method can be used to reorder the columns of a DataFrame by name.
