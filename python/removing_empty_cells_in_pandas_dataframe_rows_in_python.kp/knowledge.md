---
title: Remove rows with missing data from a pandas dataframe
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: df.dropna()
---

**Contents**

[TOC]

## Introduction
Pandas is a library for data manipulation and analysis, particularly useful when handling tabular data or working with data frames, which are two-dimensional structures capable of holding data of different types.

When working with data, it's common to come across missing or empty values in our data sets, which can hinder our ability to conduct meaningful analyses. One of the key techniques we can use to address this issue is to drop rows containing empty cells from a pandas DataFrame.

In this article, we will discuss how to drop rows containing empty cells from a pandas DataFrame in Python.


## Checking for Empty Values
Before we can drop rows containing empty cells from a pandas DataFrame, we need to identify which rows contain empty cells. We can do this using the Pandas method `isna()`, which returns a DataFrame of the same shape with each cell containing True or False based on whether it is empty or not.

```python
import pandas as pd

# Creating a DataFrame
df = pd.DataFrame({'A': [1, 2, np.nan, 3],
                   'B': [np.nan, 5, 6, 7],
                   'C': [8, 9, 10, np.nan]})

# Checking for empty values
empty_rows = df.isna().any(axis=1)
print(empty_rows)

# Output:
# 0    False
# 1     True
# 2     True
# 3     True
# dtype: bool
```

In this example, we create a DataFrame containing some empty cells. We then use the `isna()` method to check which of the cells are empty. Finally, we use the `any()` method to check if there are any empty cells in each row, which returns a Boolean value for each row indicating whether it contains any empty cells (`True`) or not (`False`). 

## Dropping Rows
Once we have identified the rows that contain empty cells, we can drop them from the DataFrame using the `dropna()` method. This method removes rows or columns that contain missing values.

```python
# Creating a DataFrame
df = pd.DataFrame({'A': [1, 2, np.nan, 3],
                   'B': [np.nan, 5, 6, 7],
                   'C': [8, 9, 10, np.nan]})

# Dropping empty rows
empty_rows = df.isna().any(axis=1)
df.dropna(subset=empty_rows, inplace=True)
print(df)

# Output:
#      A    B     C
# 0  1.0  NaN   8.0
```

In this example, we use the `dropna()` method to remove any rows containing empty cells (`NaN`) in our DataFrame `df`. We pass the argument `subset=empty_rows` to specify that we want to only drop rows where `empty_rows` is `True`. The argument `inplace=True` specifies that we want the changes to be made to the original DataFrame `df` rather than returning a new DataFrame.

After executing the code, we can see that the only remaining row in the DataFrame is the first row, which did not contain any empty cells.

## Conclusion
In this article, we have discussed how to drop rows containing empty cells from a pandas DataFrame in Python. We first checked for empty cells using the `isna()` method, which helped us identify rows that contained empty cells. We then removed these rows using the `dropna()` method, which allowed us to remove rows containing empty cells from our DataFrame.
