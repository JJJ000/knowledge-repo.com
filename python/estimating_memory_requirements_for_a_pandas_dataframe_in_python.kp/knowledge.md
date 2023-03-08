---
title: What is the method to approximate the amount of memory that a pandas dataframe will require?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: One way to estimate how much memory a Pandas` DataFrame will need in Python is to use the .memory\_usage() method to calculate the memory usage of each column and sum them up.
---

**Contents**

[TOC]

## Introduction

Pandas' DataFrame is a powerful data structure of Python. It is used for data manipulation and data analysis. Sometimes, we may need to estimate the memory size, which a DataFrame will occupy in Python. In this tutorial, we will discuss how we can estimate the memory usage of a Pandas DataFrame.

## Determining the size of DataFrame

We can estimate the memory usage of a DataFrame by determining the size of DataFrame. We can use the `size` attribute of the DataFrame to get the total number of elements in the DataFrame. We can also use the `memory_usage` method of the DataFrame to get the memory usage of each column.

```python
import pandas as pd

df = pd.read_csv('data.csv')

# Get the size of the DataFrame
size = df.size

# Get the memory usage of each column
mem_usage = df.memory_usage(deep=True)
```

In the above code, we first read a CSV file and create a DataFrame. We then use the `size` attribute of the DataFrame to get the total number of elements in the DataFrame. We also use the `memory_usage` method of the DataFrame to get the memory usage of each column. The `deep` parameter of the `memory_usage` method is set to `True` to get the memory usage of each element in the DataFrame.

## Calculating memory usage

Once we have determined the size of the DataFrame and the memory usage of each column, we can calculate the total memory usage of the DataFrame. We can do this by multiplying the size of the DataFrame with the size of each element in the DataFrame. We can then add the memory usage of each column to get the total memory usage of the DataFrame.

```python
total_mem_usage = size * df.values.itemsize
total_mem_usage += mem_usage.sum()

print(f"Total memory usage: {total_mem_usage / 1024 / 1024:.2f} MB")
```

In the above code, we calculate the total memory usage of the DataFrame by multiplying the size of the DataFrame with the size of each element in the DataFrame. We then add the memory usage of each column to get the total memory usage of the DataFrame. Finally, we print the total memory usage of the DataFrame in MB.

## Conclusion

In this tutorial, we discussed how to estimate the memory usage of a Pandas DataFrame. We first determined the size of the DataFrame and the memory usage of each column. We then calculated the total memory usage of the DataFrame by multiplying the size of the DataFrame with the size of each element in the DataFrame and adding the memory usage of each column.
