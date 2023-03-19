---
title: Groupby of pandas columns containing nan (absent) values
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: By default, pandas groupby() function excludes NaN values, but we can include them by specifying the parameter dropna=False.
---

**Contents**

[TOC]

# Introduction
When working with data, it is common to encounter missing values, represented in Pandas as NaN (Not a Number). These values can make it difficult to, for example, group data by specific columns, which is a common task in data analysis. In this tutorial, we will explore ways to group Pandas DataFrames by columns containing NaN values.


# Creating a Sample DataFrame

First, let's create a sample DataFrame with some NaN values in it:

```python
import pandas as pd
import numpy as np

data = {
    'A': [1, 1, 2, 2, 3, 3],
    'B': [np.nan, 2, np.nan, 4, 5, np.nan],
    'C': [6, 7, 8, 9, 10, 11]
}

df = pd.DataFrame(data)
```

This will create a DataFrame with three columns (`A`,`B`, and `C`), and six rows, where some values in column `B` are missing.


# Grouping by Columns with NaN Values

To group by columns with NaN values, you can simply pass the column name to the `groupby()` method. For example, to group by column `B`, you can do:

```python
grouped = df.groupby('B')
```

This will group the rows in the DataFrame using the values in column `B`, including the NaN values. The resulting `grouped` object can be used to perform various functions on the groups, such as applying a function to each group or aggregating the groups into new DataFrames.


# Handling NaN Values in GroupBy Operations

When applying functions to groups with NaN values, it is important to handle the NaN values properly to get the desired results. One approach is to use the `dropna()` method to remove any rows containing NaN values before applying the function. For example, to apply the `sum()` function to groups in column `B`, you can do:

```python
grouped = df.dropna().groupby('B')
total_sum = grouped['C'].sum()
```

This will remove any rows in the DataFrame containing NaN values in column `B`, and then group the remaining rows by the values in `B`. Finally, it will calculate the sum of the `C` column for each group.

Another approach is to replace NaN values with a specific value before applying the function. For example, to replace NaN values in column `B` with `0`, you can do:

```python
df.fillna(0, inplace=True)
grouped = df.groupby('B')
total_sum = grouped['C'].sum()
```

This will replace NaN values in column `B` with `0`, group the rows by the values in `B`, and calculate the sum of the `C` column for each group.

# Conclusion

In this tutorial, we explored ways to group Pandas DataFrames by columns containing NaN values. We saw that it is possible to group by columns with NaN values by simply passing the column name to the `groupby()` method. However, when applying functions to groups with NaN values, it is important to handle the NaN values properly, either by removing them with `dropna()` or by replacing them with a specific value with `fillna()`.
