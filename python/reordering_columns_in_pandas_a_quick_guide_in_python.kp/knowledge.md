---
title: Change the order of columns in a pandas dataframe
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: To set order of columns in a pandas dataframe in Python, use the reindex() method and pass a list of columns in the desired order as argument.
---

**Contents**

[TOC]

## 1. Introduction
When working with data in pandas, it is often necessary to rearrange the order of columns in a DataFrame. For example, you may want to move a particular column to the front or rear of the DataFrame, or you may want to swap the positions of two columns. In this tutorial, we will explore various methods for changing the order of columns in a pandas DataFrame.

## 2. Selecting and reordering columns
The easiest way to reorder columns in a pandas DataFrame is to select a subset of columns and specify their desired order. To do this, we use the `.loc` accessor and pass in the columns we want, in the desired order. For example, to move the "b" column to the front of the DataFrame, we can write:

```
df = df.loc[:, ['b'] + [col for col in df.columns if col != 'b']]
```

Here, we pass in a list containing the column 'b' followed by all other columns. This creates a new DataFrame with the columns in the desired order.

## 3. Using the .loc accessor with slice notation
Alternatively, we can use slice notation with the `.loc` accessor to reorder columns. For example, to move the last column to the front of the DataFrame, we can write:

```
df = df.loc[:, ['z'] + list(df.columns[:-1])]
```

Here, we pass in a list containing the last column 'z' followed by all other columns except for the last one.

## 4. Using the .iloc accessor
Another way to reorder columns in a pandas DataFrame is to use the `.iloc` accessor, which works with integer indices rather than labels. For example, to swap the positions of the first two columns, we can write:

```
df = df.iloc[:, [1, 0] + list(range(2, len(df.columns)))]
```

Here, we pass in a list containing the indices of the columns we want to swap, followed by a range object containing the indices of the remaining columns.

## Conclusion
Changing the order of columns in a pandas DataFrame is a common operation that can be accomplished using a variety of methods, including selecting and reordering columns, using the `.loc` and `.iloc` accessors with slice notation, and using the `.iloc` accessor with integer indices. By selecting the appropriate method for your use case, you can easily manipulate the structure of your data to suit your needs.
