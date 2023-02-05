---
title: How to select specific columns from a pandas dataframe
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: To take column-slices of a dataframe in pandas, use the DataFrame.loc[, column\_slice] syntax.
---

**Contents**

[TOC]

## 1. Selecting a Single Column

The simplest way to take a column-slice of a dataframe is to select a single column. This can be done by passing the column name as a string to the dataframe:

```python
df['column_name']
```

## 2. Using `.loc`

The `.loc` method can be used to select multiple columns by passing in a list of column names:

```python
df.loc[:, ['column_name_1', 'column_name_2']]
```

## 3. Using `.iloc`

The `.iloc` method can be used to select multiple columns by passing in a list of column indices:

```python
df.iloc[:, [0, 1]]
```

## 4. Using `.ix`

The `.ix` method can be used to select multiple columns by passing in a list of column names or indices:

```python
df.ix[:, ['column_name_1', 'column_name_2']]
```
