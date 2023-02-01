---
title: What is the process for converting a hierarchical index in columns to a single level?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the pandas.DataFrame.reset\_index() method to flatten a hierarchical index in columns.
---

**Contents**

[TOC]

**Section 1: Using the reset_index() Method**

The easiest way to flatten a hierarchical index in columns is to use the `reset_index()` method. This method converts the hierarchical index into a regular index, and moves all the columns from the hierarchical index into the dataframe as regular columns.

**Section 2: Example**

For example, consider the following dataframe:

```
import pandas as pd

df = pd.DataFrame({'A': {('a', 'x'): 1, ('a', 'y'): 2, ('b', 'x'): 3, ('b', 'y'): 4},
                   'B': {('a', 'x'): 5, ('a', 'y'): 6, ('b', 'x'): 7, ('b', 'y'): 8}})

df = df.set_index(['A', 'B'])

df
    A  B
a x  1  5
  y  2  6
b x  3  7
  y  4  8
```

Using the `reset_index()` method, we can flatten the hierarchical index:

```
df.reset_index()

   A  B  A  B
0  a  x  1  5
1  a  y  2  6
2  b  x  3  7
3  b  y  4  8
```

**Section 3: Parameters**

The `reset_index()` method takes two optional parameters: `level` and `drop`. The `level` parameter can be used to specify which level of the hierarchical index should be reset. The `drop` parameter can be used to specify whether the column labels should be dropped or not.

**Section 4: Conclusion**

In conclusion, the `reset_index()` method is an easy way to flatten a hierarchical index in columns. It takes two optional parameters, `level` and `drop`, that can be used to specify which level of the index should be reset and whether the column labels should be dropped or not.
