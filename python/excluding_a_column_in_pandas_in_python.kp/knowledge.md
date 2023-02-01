---
title: What is the syntax for selecting all columns in pandas except one?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the `.drop()` method to select all columns except one in pandas.
---

**Contents**

[TOC]

**Section 1: Using `.drop()`**

The `.drop()` method can be used to select all columns except one in pandas. This method takes in the column name as an argument and returns a new dataframe with the column dropped. 

For example, if we wanted to select all columns except the 'Name' column:

```
df = df.drop('Name', axis=1)
```

**Section 2: Using `.loc`**

The `.loc` indexer can also be used to select all columns except one in pandas. This method takes in the column name as an argument and returns a new dataframe with the column dropped. 

For example, if we wanted to select all columns except the 'Name' column:

```
df = df.loc[:, df.columns != 'Name']
```

**Section 3: Using `.iloc`**

The `.iloc` indexer can also be used to select all columns except one in pandas. This method takes in the column index as an argument and returns a new dataframe with the column dropped. 

For example, if we wanted to select all columns except the 'Name' column, which is at index 0:

```
df = df.iloc[:, df.columns != 0]
```

**Section 4: Using `list comprehension`**

List comprehension can also be used to select all columns except one in pandas. This method takes in the column name as an argument and returns a new dataframe with the column dropped. 

For example, if we wanted to select all columns except the 'Name' column:

```
df = df[[column for column in df.columns if column != 'Name']]
```
