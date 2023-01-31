---
title: How to use 'in' and 'not in' to select or exclude data from a pandas dataframe, similar to how it is used in sql
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Use the Pandas` query() method to filter a Pandas dataframe using `in` and `not in` like in SQL in Python.
---

**Contents**

[TOC]

### Using 'in'
The `in` operator in Pandas can be used to filter a dataframe based on a list of values. To use the `in` operator, we can use the syntax `df[df.column.isin(list_of_values)]`.

For example, if we have a dataframe `df` with a column `color` that contains values `red`, `green`, and `blue`, we can filter the dataframe to only include rows with the color `red` using the following command:

```
df[df.color.isin(['red'])]
```

### Using 'not in'
The `not in` operator in Pandas can be used to filter a dataframe based on a list of values that should not be included. To use the `not in` operator, we can use the syntax `df[~df.column.isin(list_of_values)]`.

For example, if we have a dataframe `df` with a column `color` that contains values `red`, `green`, and `blue`, we can filter the dataframe to exclude rows with the color `red` using the following command:

```
df[~df.color.isin(['red'])]
```

### Combining 'in' and 'not in'
We can also combine the `in` and `not in` operators to filter a dataframe based on multiple lists of values. To combine the `in` and `not in` operators, we can use the syntax `df[(df.column.isin(list_of_values_1)) & (~df.column.isin(list_of_values_2))]`.

For example, if we have a dataframe `df` with a column `color` that contains values `red`, `green`, and `blue`, we can filter the dataframe to only include rows with the colors `green` and `blue` using the following command:

```
df[(df.color.isin(['green', 'blue'])) & (~df.color.isin(['red']))]
```
