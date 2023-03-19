---
title: What's the way to pick unique values from multiple data frame columns in pandas?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: Use the `drop\_duplicates` method with the `subset` parameter set to a list of multiple column names.
---

**Contents**

[TOC]

## Introduction
In Pandas library, we can use the `drop_duplicates()` method to select distinct values from a single column. However, if we want to select unique values across multiple columns, we need to use a different approach. In this tutorial, we will discuss how we can use the `groupby()` method to select distinct values across multiple columns in a Pandas DataFrame in Python.

## Import Required Libraries
Before we start working with Pandas, we need to import the required libraries. The following command imports the required libraries for our task.

```python
import pandas as pd
```

## Select distinct values across multiple columns
We can use the `groupby()` method in Pandas to select distinct values across multiple columns. We can pass a list of column names to the `groupby()` method to group the DataFrame by those columns. After grouping the DataFrame, we can retrieve the first row from each group to get the distinct values. The following code demonstrates this approach.

```python
df = pd.DataFrame({
    'A': ['foo', 'foo', 'bar', 'bar', 'foo'],
    'B': ['one', 'one', 'two', 'two', 'one'],
    'C': [1, 1, 2, 2, 3]
})

distinct_df = df.groupby(['A', 'B'])['C'].first().reset_index()
```

In the above code, we have created a DataFrame `df` with three columns `A`, `B`, and `C`. We then group the DataFrame by columns `A` and `B` using the `groupby()` method. After that, we retrieve the first row of each group using the `first()` method and select only the `C` column. Finally, we reset the index of the resulting DataFrame to get the distinct values across multiple columns.


## Conclusion
In this tutorial, we have learned how to select distinct values across multiple columns in a Pandas DataFrame in Python. We have used the `groupby()` method to group the DataFrame by the columns of interest and retrieve the first row of each group to get the distinct values.
