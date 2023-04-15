---
title: Merging pandas dataframes based on the names of their columns
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Use the `merge()` function in pandas to join DataFrames by their column names.
---

**Contents**

[TOC]

## Section 1: Introduction

Pandas is a powerful library in Python used for data manipulation, analysis, and cleaning. One of its most useful features is the ability to merge two DataFrames. This can be done in many ways, but one of the most popular ways is to join DataFrames based on their column names. In this tutorial, we will show you how to join pandas DataFrames by column names in Python.


## Section 2: Using pd.merge()

The easiest way to join DataFrames in pandas is by using the pd.merge() method. This method is very simple to use and is great when both DataFrames have the same column names that you would like to merge on. Here’s an example of how to use pd.merge():

```python
import pandas as pd
 
# Create two sample DataFrames
df1 = pd.DataFrame({'customer': ['A', 'B', 'C', 'D'],
                   'field1': [1, 2, 3, 4],
                   'field2': [5, 6, 7, 8]})
 
df2 = pd.DataFrame({'customer': ['A', 'B', 'E', 'F'],
                   'field3': [9, 10, 11, 12],
                   'field4': [13, 14, 15, 16]})

# Merge the two DataFrames on 'customer'
merged_df = pd.merge(df1, df2, on='customer')

print(merged_df)
```

In the code above, we first create two sample DataFrames, df1 and df2. We then merge them using pd.merge() by specifying the ‘customer’ column name. This column is common to both DataFrames and acts as the “joining column”. The resulting merged DataFrame contains rows where the ‘customer’ column matches between df1 and df2.

## Section 3: Using Join()

Another way to join DataFrames in pandas is by using the .join() method. This method is similar to pd.merge() but requires that the DataFrames have a common index. Here’s an example of how to use .join():

```python
import pandas as pd

# Create two sample DataFrames
df1 = pd.DataFrame({'field1': [1, 2, 3, 4], 'field2': [5, 6, 7, 8]}, 
                   index=['A', 'B', 'C', 'D'])

df2 = pd.DataFrame({'field3': [9, 10, 11, 12], 'field4': [13, 14, 15, 16]},
                   index=['A', 'B', 'E', 'F'])

merged_df = df1.join(df2)

print(merged_df)
```

In the code above, we create two sample DataFrames, df1 and df2, with a common index. We then join them using the .join() method. This method combines the two DataFrames based on the index, i.e. the rows in the resulting DataFrame correspond to rows with matching indices in the original DataFrames.

## Section 4: Conclusion

Joining pandas DataFrames by column names in Python is a simple process. The pandas library provides various methods to merge DataFrames using a common column or index. Among these methods, pd.merge() and .join() are the simplest and most commonly used, especially when joining DataFrames with common column names or indices.
