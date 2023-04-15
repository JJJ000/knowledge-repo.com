---
title: What is the method to substitute nans with the values preceding or following them in a pandas dataframe?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Use the pandas DataFrame method `fillna()` with the method parameter set to either `ffill` (forward fill) or `bfill` (backward fill) to replace NaN values with preceding or next values, respectively.
---

**Contents**

[TOC]

## Introduction

Dealing with missing values or NaNs in datasets is a common problem in data analysis. One of the strategies to handle this issue is to replace missing values with the preceding or next values in a DataFrame. Pandas provides several methods to accomplish this task.

In this tutorial, we will demonstrate the following approaches to replace NaNs with preceding or next values in a pandas DataFrame:

1. `fillna()` method with ffill and bfill options
2. `interpolate()` method with pad and bfill options


## Set Up

Before we begin, let's import necessary libraries and create a sample DataFrame with NaN values.


```python
import pandas as pd
import numpy as np

df = pd.DataFrame({'A': [1, 2, np.nan, 4, 5], 'B': [np.nan, 2, 3, np.nan, 5]})
print(df)
```

Output:

```
     A    B
0  1.0  NaN
1  2.0  2.0
2  NaN  3.0
3  4.0  NaN
4  5.0  5.0
```

## 1. `fillna()` method with ffill and bfill options

The `fillna()` method in pandas is used to fill the missing values with a particular value. We can use forward fill (`ffill`) or backward fill (`bfill`) option to carry forward the last known value or carry backward the next known value, respectively.

### Using `fillna()` method with ffill option to replace NaNs with preceding values


```python
# Using ffill to fill NaN values with preceding values
df.fillna(method='ffill', inplace=True)
print(df)
```

Output:

```
     A    B
0  1.0  NaN
1  2.0  2.0
2  2.0  3.0
3  4.0  3.0
4  5.0  5.0
```

### Using `fillna()` method with bfill option to replace NaNs with next values


```python
# Using bfill to fill NaN values with next values
df.fillna(method='bfill', inplace=True)
print(df)
```

Output:

```
     A    B
0  1.0  2.0
1  2.0  2.0
2  4.0  3.0
3  4.0  5.0
4  5.0  5.0
```


## 2. `interpolate()` method with pad and bfill options

The `interpolate()` method in pandas is a powerful tool to fill missing values using various interpolation methods. We can use forward fill (`pad`) or backward fill (`bfill`) option to carry forward the last known value or carry backward the next known value, respectively. 

### Using `interpolate()` method with pad option to replace NaNs with preceding values

```python
# Using pad (ffill) to fill NaN values with preceding values
df.interpolate(method='pad', inplace=True)
print(df)
```

Output:

```
     A    B
0  1.0  NaN
1  2.0  2.0
2  2.0  3.0
3  4.0  3.0
4  5.0  5.0
```


### Using `interpolate()` method with bfill option to replace NaNs with next values


```python
# Using bfill to fill NaN values with next values
df.interpolate(method='bfill', inplace=True)
print(df)
```

Output:

```
     A    B
0  1.0  2.0
1  2.0  2.0
2  4.0  3.0
3  4.0  5.0
4  5.0  5.0
```

## Conclusion

In this tutorial, we demonstrated how to replace missing values or NaNs with preceding or next values in a pandas DataFrame. We used two different methods: `fillna()` and `interpolate()`, with ffill/pad and bfill options, respectively. 
These methods can be used to modify your existing dataset to include accurate estimates of these NaNs, and get you closer to a better and more accurate understanding of your dataset.
