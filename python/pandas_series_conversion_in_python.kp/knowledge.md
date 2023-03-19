---
title: Transform a pandas series into a dataframe
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: To convert a pandas Series to a DataFrame in Python, use the to\_frame() method.
---

**Contents**

[TOC]

## Introduction

Pandas is an open-source data manipulation tool for Python. It provides high-performance, easy-to-use data structures for data analysis. One of the most commonly used data structures in pandas is the Series object. In this tutorial, we will discuss how to convert a pandas Series to a DataFrame.

## Creating a Series object

Before we discuss how to convert a Series to a DataFrame, let's first create a Series object. We can create a Series object by passing a list of values to the pandas Series constructor. 

```python
import pandas as pd

# create a Series
series = pd.Series([10, 20, 30, 40, 50])
print(series)
```

Output:

```
0    10
1    20
2    30
3    40
4    50
dtype: int64
```

## Converting a Series to a DataFrame

Converting a Series to a DataFrame is a simple process. We can use the `to_frame()` method to convert a Series to a DataFrame. Here's how:

```python
# convert Series to DataFrame
df = series.to_frame()
print(df)
```

Output:

```
    0
0  10
1  20
2  30
3  40
4  50
```

By default, the `to_frame()` method will create a DataFrame with a single column. The name of the column will be the name of the Series. In this case, the name of the column is `0`.

If we want to rename the column, we can set the `columns` parameter of the `to_frame()` method to the desired name:

```python
# convert Series to DataFrame with a renamed column
df = series.to_frame("numbers")
print(df)
```

Output:

```
   numbers
0       10
1       20
2       30
3       40
4       50
```

In this example, we created a DataFrame with a single column named `numbers`.

## Conclusion 

Converting a pandas Series to a DataFrame is a simple process that can be done using the `to_frame()` method. This method creates a DataFrame with a single column by default, but we can rename the column by setting the `columns` parameter of the method.
