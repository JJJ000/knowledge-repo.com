---
title: Groupby two columns in a pandas dataframe and obtain the number of occurrences
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Use the Pandas groupby function with two columns and the count() method.
---

**Contents**

[TOC]

Section 1: Introduction
----------------------
Pandas is a widely used open-source data analysis and manipulation library for Python. One of the most powerful features of Pandas is the ability to group data by certain criteria and perform calculations on the grouped data. In this tutorial, we will explore groupby function in pandas to group a dataframe by two columns and get counts of each group of rows.


Section 2: Grouping a dataframe by two columns
----------------------------------------------
In order to group a dataframe by two columns, we need to use the 'groupby' method on the dataframe and pass a list of column names to group by. For example, if we have a dataframe 'df' with two columns 'A' and 'B', we can group the dataframe by these two columns as shown below:

``` python
grouped_df = df.groupby(['A', 'B'])
```

The resulting object 'grouped_df' is a GroupBy object which can be used to perform various aggregation operations on the grouped data.


Section 3: Getting counts of each group
--------------------------------------
Once we have a GroupBy object, we can use the 'size' method to get the counts of each group. The 'size' method returns a Series object with the counts of each group. For example, to get the counts of each group in our grouped dataframe 'grouped_df', we can call the 'size' method as shown below:

``` python
counts = grouped_df.size()
```

The resulting Series object 'counts' contains the counts of each group. The index of the Series object contains the unique values of the group columns in tuples.


Section 4: Example usage
------------------------
Let us consider an example to illustrate the above concepts. Suppose we have a dataframe 'sales' with columns 'region', 'product' and 'sales_amount'. We want to group the dataframe by 'region' and 'product', and get the counts of each group. We can do this as follows:

``` python
grouped_sales = sales.groupby(['region', 'product'])
counts = grouped_sales.size()
print(counts)
```

The output will be a Series object with counts of each group of rows in the dataframe grouped by 'region' and 'product'.
