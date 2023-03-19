---
title: The method fillna() in pandas dataframe can replace null values in specific columns only, directly modifying the original object
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: To fill only some columns in place in a Pandas dataframe, chain the column names with fillna() and pass a dictionary with the column name and the desired fill value to the method.
---

**Contents**

[TOC]

## Introduction

In Python, `pandas` is a library that is widely used in data science and data analysis. It provides tools for manipulating and analyzing data in a tabular or structured format using data structures such as a `Series` or `DataFrame`. One of the common operations performed while working with data is handling missing data, often represented by NaN (Not a Number) values in pandas. The `fillna` method is used to handle missing data by filling NaN values with a specified value or by applying a function across the missing values. In this article, I will demonstrate how to fill NaN values in only some columns of a pandas DataFrame in place.

## Creating Sample DataFrame

Let's start by creating a sample DataFrame to illustrate the `fillna()` method of pandas. We will create a DataFrame `df` with three columns - `Name`, `Age`, and `Salary`.

```python
import pandas as pd
import numpy as np

df = pd.DataFrame({'Name': ['Alice', 'Bob', 'Charlie', 'David'],
                   'Age': [20, np.NaN, 25, np.NaN],
                   'Salary': [5000, 4500, np.NaN, 6200]})
```

## Filling NaN Values in Only Some Columns

To fill NaN values in only some columns of a pandas DataFrame using the `fillna()` method, we will specify the columns that we want to fill. For instance, let's say we want to fill NaN values only in the `Age` column with a default value of 0.

```python
df['Age'].fillna(0, inplace=True)
```

Here, we have specified the column `Age` and filled NaN values with a default value of 0, by setting the second parameter of the `fillna()` method to `0`. The `inplace=True` flag ensures that the changes are made in place, i.e., the original DataFrame is updated with the new values.

Similarly, let's say we want to fill NaN values only in the `Salary` column with the average value of the `Salary` column.

```python
mean_salary = df['Salary'].mean()
df['Salary'].fillna(mean_salary, inplace=True)
```

Here, we have specified the column `Salary` and filled NaN values with the average value of the `Salary` column, which we have calculated and stored in the `mean_salary` variable. Again, the `inplace=True` flag ensures that the changes are made in place, i.e., the original DataFrame is updated with the new values.

## Filling NaN Values in Multiple Columns

We can also fill NaN values in multiple columns by specifying a list of columns. For instance, let's say we want to fill NaN values in both the `Age` and `Salary` columns simultaneously.

```python
df[['Age', 'Salary']].fillna(0, inplace=True)
```

Here, we have specified a list of columns `['Age', 'Salary']` and filled NaN values with a default value of 0. Again, the `inplace=True` flag ensures that the changes are made in place, i.e., the original DataFrame is updated with the new values.

## Conclusion

In this article, we have learned how to fill NaN values in only some columns of a pandas DataFrame using the `fillna()` method. We have seen how to fill NaN values in a single column as well as in multiple columns. We hope this helps you in your data analysis and manipulation tasks using pandas.
