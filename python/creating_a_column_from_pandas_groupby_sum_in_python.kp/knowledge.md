---
title: What is the process for generating a fresh column using the result of pandas groupby().sum()?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Assign the output of the groupby().sum() method to a new column in the dataframe using the [] operator with the column name in quotes as the key.
---

**Contents**

[TOC]

Introduction
------------
When analyzing data with pandas in Python, one often groups the data by certain criteria to calculate summary statistics. The pandas `groupby().sum()` function is commonly used to obtain the sum of a particular column for each unique value in another column. However, after obtaining the output of `groupby().sum()`, you may wish to create a new column in the original dataframe with these calculated values. In this guide, we will discuss how to accomplish this in two ways.


Section 1: Using pandas merge() function
----------------------------------------
The easiest method to create a new column from the output of `groupby().sum()` is to use the pandas `merge()` function. Here is an example:

```
import pandas as pd

# Create sample dataframe
df = pd.DataFrame({'name':['Alice', 'Bob', 'Charlie', 'Bob', 'Charlie'], 'salary':[50000, 60000, 55000, 55000, 50000]})
print(df)

# Group by name and calculate total salary
grouped = df.groupby('name').sum().reset_index()
print(grouped)

# Merge the original dataframe with the grouped dataframe using the 'name' column
merged = pd.merge(df, grouped, on='name')

# Create new column with the normalized salary
merged['norm_salary'] = merged['salary_x'] / merged['salary_y']

print(merged)
```

In this example, we create a sample dataframe `df` with two columns - `name` and `salary`. We then group the dataframe by `name` and calculate the sum of the salaries for each unique name using `groupby().sum()`. This creates a new dataframe `grouped`, which has two columns - `name` and `salary`.

To create a new column in the original dataframe `df` with the normalized salary (i.e. salary as a fraction of the total salary for each name), we use the `merge()` function to merge `df` and `grouped` on the `name` column. This creates a new dataframe `merged` with two sets of salary columns (`salary_x` and `salary_y`). We can use these two columns to create the new `norm_salary` column.

Note that we need to reset the index of `grouped` using `.reset_index()` so that the `name` column becomes a normal column that can be used in the `merge()` function.


Section 2: Using pandas join() function
---------------------------------------
Another way to create a new column from the output of `groupby().sum()` is to use the pandas `join()` function. This works similarly to the `merge()` function. Here is an example:

```
import pandas as pd

# Create sample dataframe
df = pd.DataFrame({'name':['Alice', 'Bob', 'Charlie', 'Bob', 'Charlie'], 'salary':[50000, 60000, 55000, 55000, 50000]})
print(df)

# Group by name and calculate total salary
grouped = df.groupby('name').sum().reset_index()
print(grouped)

# Join the original dataframe with the grouped dataframe using the 'name' column
joined = df.set_index('name').join(grouped.set_index('name'), rsuffix='_total')

# Create new column with the normalized salary
joined['norm_salary'] = joined['salary'] / joined['salary_total']

print(joined.reset_index())
```

This example is very similar to the previous one, but instead of using the `merge()` function, we use the `join()` function to combine the original dataframe `df` and the grouped dataframe `grouped`. To use `join()`, we need to set the index of both dataframes to the `name` column (using `set_index()`), and then tell `join()` to use the index to join the dataframes. 

This creates a new dataframe `joined` with two sets of salary columns (`salary` and `salary_total`, which corresponds to the sum of the salaries for each name). We can use these two columns to create the new `norm_salary` column.

Note that we also need to reset the index of `joined` using `reset_index()` to transform the `name` column back into a normal column.
