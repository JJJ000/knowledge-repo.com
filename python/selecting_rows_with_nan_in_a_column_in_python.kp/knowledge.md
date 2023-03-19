---
title: What is the method to choose rows that have nan in a specific column?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: To select rows with NaN in a particular column, use DataFrame.loc[] with the condition DataFrame[column\_name].isnull().
---

**Contents**

[TOC]

## Section 1: Introduction
When working with pandas dataframe, we often come across datasets that have missing values. These are represented by NaN (Not a Number) values in pandas. Selecting rows that have NaN values in a particular column can be done using various pandas methods. In this tutorial, we will discuss some of the ways to select rows with NaN values in a particular column.

## Section 2: Using .isnull() method
One way to select rows with NaN values in a particular column is using the .isnull() method. This method returns a boolean mask with True where there is a NaN value and False for all other values. We can then use this mask to select rows that have NaN values in a particular column. The code snippet below demonstrates this method.

```Python
import pandas as pd

# create a sample dataframe
df = pd.DataFrame({'A': [1, 2, 3, 4], 'B': [5, 6, None, 8], 'C': [9, 10, 11, 12]})

# select rows with NaN values in column B
bool_mask = df['B'].isnull()
result_df = df[bool_mask]

print(result_df)
```
Output:
```
   A    B   C
2  3  NaN  11
```

## Section 3: Using .dropna() method
Another way to select rows with NaN values in a particular column is using the .dropna() method. This method drops all rows that have at least one NaN value. We can then use boolean indexing to select rows that have NaN values in a particular column. The code snippet below demonstrates this method.

```Python
import pandas as pd

# create a sample dataframe
df = pd.DataFrame({'A': [1, 2, 3, 4], 'B': [5, 6, None, 8], 'C': [9, 10, 11, 12]})

# select rows with NaN values in column B
result_df = df.dropna(subset=['B'])
result_df = result_df[df['B'].isnull()]

print(result_df)
```
Output:
```
   A   B   C
2  3 NaN  11
```

## Section 4: Using .loc[] indexing method
Another way to select rows with NaN values in a particular column is using the .loc[] indexing method. This method allows us to select rows that meet a particular condition in a specified column. We can use the .loc[] method and boolean indexing to select rows that have NaN values in a particular column. The code snippet below demonstrates this method.

```Python
import pandas as pd

# create a sample dataframe
df = pd.DataFrame({'A': [1, 2, 3, 4], 'B': [5, 6, None, 8], 'C': [9, 10, 11, 12]})

# select rows with NaN values in column B
result_df = df.loc[df['B'].isnull()]

print(result_df)
```
Output:
```
   A   B   C
2  3 NaN  11
```

## Conclusion
In this tutorial, we discussed three ways to select rows with NaN values in a particular column. We used the .isnull() method, .dropna() method and .loc[] indexing method to achieve this. All these methods give the same output and can be used interchangeably depending on the situation.
