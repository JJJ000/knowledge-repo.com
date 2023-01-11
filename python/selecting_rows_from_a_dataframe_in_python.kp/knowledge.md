---
title: What is the process for choosing rows from a dataframe based on the values of a specific column?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-11 00:00:00
updated_at: 2023-01-11 00:00:00
tldr: You can use the `DataFrame.loc[]` method to select rows based on column values.
---

**Contents**

[TOC]

### Using a Single Column Value

Using the `.loc` method, you can select rows from a DataFrame based on a single column value. For example, to select all rows where the 'name' column has the value 'Bob':

```python
df.loc[df['name'] == 'Bob']
```

### Using Multiple Column Values

Using the `.loc` method, you can also select rows from a DataFrame based on multiple column values. For example, to select all rows where the 'name' column has the value 'Bob' and the 'age' column has the value '20':

```python
df.loc[(df['name'] == 'Bob') & (df['age'] == 20)]
```

### Using the `isin` Method

You can also use the `.isin` method to select rows from a DataFrame based on multiple column values. For example, to select all rows where the 'name' column has the value 'Bob' or 'John':

```python
df.loc[df['name'].isin(['Bob', 'John'])]
```

### Using the `query` Method

You can also use the `.query` method to select rows from a DataFrame based on multiple column values. For example, to select all rows where the 'name' column has the value 'Bob' or 'John' and the 'age' column has the value '20':

```python
df.query('name in ["Bob", "John"] and age == 20')
```
