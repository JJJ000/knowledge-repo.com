---
title: Break up a sizable pandas dataframe
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Use pandas` `.split()` function with the desired split criteria to split a large dataframe into smaller dataframes in Python.
---

**Contents**

[TOC]

## Introduction

Splitting a big pandas DataFrame into smaller ones is a common operation. It can be done along a specific axis or based on certain conditions. In this article, we will go through some different methods to split a large pandas DataFrame in Python.

## Method 1: splitting based on groupby

The `groupby` method in pandas can be used to split a DataFrame into smaller ones based on values in one or more columns. We first specify the column(s) to group by and then apply a function to each group.

For example, let's say we have a DataFrame with columns "date", "country", "sales", and "profit". We want to split the DataFrame into smaller ones based on the values in the "country" column. We can do this as follows:

```python
grouped = df.groupby('country')
```

This creates a `groupby` object, which we can then iterate over to get access to the individual split DataFrames:

```python
for country, data in grouped:
    print(country)
    print(data)
```

This will print the name of each country and the corresponding split DataFrame.

## Method 2: splitting based on row indices

If you want to split a DataFrame into smaller ones based on row indices, you can use the `iloc` DataFrame accessor. This allows you to slice a DataFrame using integer indices.

For example, let's say we have a DataFrame with 100 rows and we want to split it into 4 smaller DataFrames of 25 rows each. We can do this as follows:

```python
df1 = df.iloc[:25]
df2 = df.iloc[25:50]
df3 = df.iloc[50:75]
df4 = df.iloc[75:]
```

This creates four new DataFrames that contain the first 25 rows, the next 25 rows, and so on.

## Method 3: splitting based on column values

You can use boolean indexing to split a DataFrame into smaller ones based on certain column values. This method is especially useful when you want to extract specific rows based on a condition.

For example, let's say we have a DataFrame with columns "date", "sales", and "profit". We want to split the DataFrame into smaller ones based on the values in the "sales" column. We can do this as follows:

```python
df_low_sales = df[df['sales'] < 1000]
df_med_sales = df[(df['sales'] >= 1000) & (df['sales'] < 5000)]
df_high_sales = df[df['sales'] >= 5000]
```

This creates three new DataFrames that contain the rows where the "sales" values are less than 1000, between 1000 and 5000, and over 5000, respectively.

## Conclusion

There are several ways to split a large pandas DataFrame into smaller ones in Python. The `groupby` method is useful if you want to split based on specific column values, while `iloc` is useful if you want to split based on row indices. Boolean indexing can be used to extract specific rows based on conditions.
