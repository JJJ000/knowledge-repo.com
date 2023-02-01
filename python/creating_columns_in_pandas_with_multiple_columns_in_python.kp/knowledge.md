---
title: Create a new column in a pandas dataframe by applying a function to multiple columns, row-wise
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: You can use the Pandas apply() function to apply a function to each row of a DataFrame, using values from multiple columns as inputs.
---

**Contents**

[TOC]

**Section 1: Create a New Column**

We can create a new column in a Pandas DataFrame using the `.assign()` method. This method takes a keyword argument of the new column name and the value that should be assigned to the new column. For example, let's say we have a DataFrame with two columns, 'A' and 'B', and we want to create a third column 'C' that is the sum of 'A' and 'B':

```python
df = df.assign(C = df['A'] + df['B'])
```

**Section 2: Apply a Function to Columns**

We can also apply a function to multiple columns of a DataFrame row-wise using the `.apply()` method. This method takes a function and applies it to each row of the DataFrame. For example, let's say we have a DataFrame with three columns, 'A', 'B', and 'C', and we want to create a fourth column 'D' that is the product of 'A', 'B', and 'C':

```python
def product(row):
    return row['A'] * row['B'] * row['C']

df = df.assign(D = df.apply(product, axis=1))
```

**Section 3: Using Lambda Expressions**

We can also use lambda expressions to apply a function to multiple columns of a DataFrame row-wise. This is useful when the function is simple and can be written in one line. For example, let's say we have a DataFrame with three columns, 'A', 'B', and 'C', and we want to create a fourth column 'D' that is the sum of 'A', 'B', and 'C':

```python
df = df.assign(D = df.apply(lambda row: row['A'] + row['B'] + row['C'], axis=1))
```

**Section 4: Using .applymap()**

Finally, we can also use the `.applymap()` method to apply a function to multiple columns of a DataFrame row-wise. This is useful when the function is more complex and cannot be written in one line. For example, let's say we have a DataFrame with three columns, 'A', 'B', and 'C', and we want to create a fourth column 'D' that is the sum of the squares of 'A', 'B', and 'C':

```python
def sum_squares(row):
    return row['A']**2 + row['B']**2 + row['C']**2

df = df.assign(D = df.applymap(sum_squares, axis=1))
```
