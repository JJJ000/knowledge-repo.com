---
title: Join a group of pandas dataframes into one
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Use the pandas `concat()` function to concatenate a list of dataframes vertically or horizontally.
---

**Contents**

[TOC]

## Introduction

In pandas, we can concatenate dataframes and combine them into a larger dataframe in a variety of ways. We'll walk through the process of concatenating dataframes using pandas' `concat()` function.

## Example dataframes

Let's start by creating two example dataframes that we'll use for demonstration:

```python
import pandas as pd

df1 = pd.DataFrame({'A': ['A0', 'A1', 'A2', 'A3'],
                    'B': ['B0', 'B1', 'B2', 'B3'],
                    'C': ['C0', 'C1', 'C2', 'C3'],
                    'D': ['D0', 'D1', 'D2', 'D3']},
                   index=[0, 1, 2, 3])

df2 = pd.DataFrame({'A': ['A4', 'A5', 'A6', 'A7'],
                    'B': ['B4', 'B5', 'B6', 'B7'],
                    'C': ['C4', 'C5', 'C6', 'C7'],
                    'D': ['D4', 'D5', 'D6', 'D7']},
                   index=[4, 5, 6, 7])
```

## Concatenating dataframes vertically

We can concatenate dataframes vertically using `concat()` function by setting the `axis` parameter to `0` or `'index'`. To illustrate this:

```python
vertical_concatenated_df = pd.concat([df1, df2])
print(vertical_concatenated_df)
```

The output of the code above will be:

```
    A   B   C   D
0  A0  B0  C0  D0
1  A1  B1  C1  D1
2  A2  B2  C2  D2
3  A3  B3  C3  D3
4  A4  B4  C4  D4
5  A5  B5  C5  D5
6  A6  B6  C6  D6
7  A7  B7  C7  D7
```

## Concatenating dataframes horizontally

We can also concatenate dataframes horizontally using `concat()` by setting the `axis` parameter to `1` or `'columns'`. To demonstrate this:

```python
horizontal_concatenated_df = pd.concat([df1, df2], axis=1)
print(horizontal_concatenated_df)
```

The output of the code above will return:

```
    A   B   C   D   A   B   C   D
0  A0  B0  C0  D0  NaN NaN NaN NaN
1  A1  B1  C1  D1  NaN NaN NaN NaN
2  A2  B2  C2  D2  NaN NaN NaN NaN
3  A3  B3  C3  D3  NaN NaN NaN NaN
4 NaN NaN NaN NaN  A4  B4  C4  D4
5 NaN NaN NaN NaN  A5  B5  C5  D5
6 NaN NaN NaN NaN  A6  B6  C6  D6
7 NaN NaN NaN NaN  A7  B7  C7  D7
```

Notice how the concatenated dataframe has duplicate column names. We can avoid this by using the `keys` parameter to set custom column names:

```python
horizontal_concatenated_df = pd.concat([df1, df2], axis=1, keys=['df1', 'df2'])
print(horizontal_concatenated_df)
```

The output of the code above will return:

```
   df1            df2           
    A   B   C   D   A   B   C   D
0  A0  B0  C0  D0  NaN NaN NaN NaN
1  A1  B1  C1  D1  NaN NaN NaN NaN
2  A2  B2  C2  D2  NaN NaN NaN NaN
3  A3  B3  C3  D3  NaN NaN NaN NaN
4 NaN NaN NaN NaN  A4  B4  C4  D4
5 NaN NaN NaN NaN  A5  B5  C5  D5
6 NaN NaN NaN NaN  A6  B6  C6  D6
7 NaN NaN NaN NaN  A7  B7  C7  D7
```


## Conclusion

We've illustrated how to concatenate dataframes vertically and horizontally using pandas' `concat()` function. By concatenating dataframes, we can easily combine data from different sources into a bigger dataframe for analysis, cleaning or visualization.
