---
title: Retrieve the initial row of every group in a pandas dataframe
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Use the `groupby` function with `head(1)` method to get the first row of each group in a pandas dataframe.
---

**Contents**

[TOC]

## Section 1: Introduction
In data analysis, it is common to group data based on one or more categorical variables and apply some operations or calculations to each group. Sometimes, we need to extract the first row of each group for further analysis or visualization.

## Section 2: Example Dataset
Let's start by creating a sample dataset using pandas library.

```python
import pandas as pd
import numpy as np

data = pd.DataFrame({'group': ['A', 'A', 'B', 'B', 'B', 'C', 'C'],
                     'value': [1, 2, 3, 4, 5, 6, 7],
                     'date': pd.date_range('20210101', periods=7)})

print(data)
```

Output:

```
  group  value       date
0     A      1 2021-01-01
1     A      2 2021-01-02
2     B      3 2021-01-03
3     B      4 2021-01-04
4     B      5 2021-01-05
5     C      6 2021-01-06
6     C      7 2021-01-07
```

## Section 3: Getting First Rows of Each Group
We can use the `groupby()` method to group the data by the "group" column and then use the `head()` method to get the first row of each group.

```python
first_rows = data.groupby('group').head(1)

print(first_rows)
```

Output:

```
  group  value       date
0     A      1 2021-01-01
2     B      3 2021-01-03
5     C      6 2021-01-06
```

As we can see, the result only contains the first row of each group.

## Section 4: Conclusion
In this tutorial, we have learned how to get the first row of each group in a pandas dataframe. We used the `groupby()` method to group the data by a categorical variable and then used the `head()` method to get the first row of each group.
