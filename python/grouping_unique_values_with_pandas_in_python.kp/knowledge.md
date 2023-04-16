---
title: Find the number of unique values in each group using pandas
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Pandas` groupby() function can be used to count unique values in groups.
---

**Contents**

[TOC]

**Section 1: Setting Up the DataFrame**

We can start by creating a sample DataFrame with some data in it.

```
import pandas as pd 

df = pd.DataFrame({'Group': ['A', 'A', 'A', 'B', 'B', 'C'],
                   'Value': [1, 1, 2, 3, 3, 4]})

print(df)
```

Output:

| Group | Value |
|-------|-------|
| A     | 1     |
| A     | 1     |
| A     | 2     |
| B     | 3     |
| B     | 3     |
| C     | 4     |

**Section 2: Count Unique Values Per Group**

We can use the `groupby` and `nunique` methods to count the unique values per group:

```
df.groupby('Group')['Value'].nunique()
```

Output:

Group
A    2
B    1
C    1
Name: Value, dtype: int64

**Section 3: Count Unique Values in Multiple Columns**

If we want to count the unique values in multiple columns, we can use the `agg` method with the `nunique` function:

```
df.groupby('Group').agg(nunique=('Value', 'nunique'))
```

Output:

| Group | nunique |
|-------|---------|
| A     | 2       |
| B     | 1       |
| C     | 1       |

**Section 4: Count Unique Values in Multiple Columns with Multiple Functions**

If we want to count the unique values in multiple columns with multiple functions, we can use the `agg` method with a list of functions:

```
df.groupby('Group').agg(nunique=('Value', 'nunique'), 
                        mean=('Value', 'mean'))
```

Output:

| Group | nunique | mean |
|-------|---------|------|
| A     | 2       | 1.33 |
| B     | 1       | 3.00 |
| C     | 1       | 4.00 |
