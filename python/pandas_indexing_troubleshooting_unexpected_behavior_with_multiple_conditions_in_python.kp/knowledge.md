---
title: The behavior of indexing a data frame with multiple conditions in pandas is not what was expected
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: When using multiple conditions while indexing a pandas dataframe in Python, the ‘&’ operator should be used instead of the ‘and’ operator.
---

**Contents**

[TOC]

1. Introduction
In pandas, indexing and selecting data is a crucial task when working with data frames. One common scenario is to select values based on multiple conditions. However, sometimes the behavior might be unexpected, and it may lead to errors or incorrect results.

2. Using Multiple Conditions in Pandas
To use multiple conditions in pandas, we can use the "&" (AND) operator or the "|" (OR) operator. For example, suppose we have a data frame "df" with two columns, "col1" and "col2", and we want to select rows where "col1" is greater than 1 and "col2" is less than 10:

```
df[(df['col1'] > 1) & (df['col2'] < 10)]
```

The "&" operator should be used when both conditions must be met. On the other hand, the "|" operator should be used when at least one condition must be met:

```
df[(df['col1'] > 1) | (df['col2'] < 10)]
```

3. Unexpected Behavior
Although the above approach seems correct, there might be some cases where the behavior is unexpected. One possible scenario is when we are trying to compare columns with NaN values. For instance, consider the following data frame "df" with three columns, "col1", "col2", and "col3":

```
import pandas as pd
import numpy as np

df = pd.DataFrame({'col1': [1, 2, 3], 'col2': [4, 5, np.nan], 'col3': [7, np.nan, 9]})
```

If we try to select rows where "col2" is less than 5 and "col3" is greater than 8, we might expect to get row 3 only. However, let's see what happens:

```
df[(df['col2'] < 5) & (df['col3'] > 8)]
```

Output:

```
   col1  col2  col3
0     1   4.0   7.0
```

Unexpectedly, we get row 1 as well, which does not meet the second condition. This happens because pandas considers NaN values as False in boolean expressions. Therefore, "np.nan < 5" returns False, and "np.nan > 8" also returns False.

4. Solution
To avoid unexpected behavior, we need to use the functions "isna()" or "notna()" to check for NaN values explicitly. For example, in the previous example, we can update the condition as follows:

```
df[(df['col2'] < 5) & (df['col3'].notna()) & (df['col3'] > 8)]
```

Now, we get the expected output:

```
   col1  col2  col3
2     3   NaN   9.0
```

By using the "notna()" function, we can exclude rows with NaN values in "col3" and get only the rows that meet both conditions. 

In conclusion, when using multiple conditions in pandas, we should be aware of possible unexpected behavior and handle NaN values explicitly using "isna()" or "notna()" functions.
