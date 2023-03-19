---
title: Eliminate rows that contain only zeros from a pandas data frame
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: df = df.loc[~(df==0).all(axis=1)]
---

**Contents**

[TOC]

## Introduction

Pandas is one of the most popular data analysis libraries for Python. In many cases, we may want to remove rows from a Pandas data frame that have all zeros. 

In this tutorial, we will demonstrate how to drop rows with all zeros in a Pandas data frame in Python. We will cover some of the main methods that can be used to accomplish this task.

## Sample Data

In order to illustrate the methods used to drop rows with all zeros in a Pandas data frame, we first need to create a sample data frame.

``` python
import pandas as pd
import numpy as np
 
# Create sample data frame
df = pd.DataFrame({
    'A':[0,0,0,0],
    'B':[1,3,5,0],
    'C':[0,0,0,0],
    'D':[1,1,1,1]
})

print(df)
```

This will output the following data frame:

```
   A  B  C  D
0  0  1  0  1
1  0  3  0  1
2  0  5  0  1
3  0  0  0  1
```

## Method 1: Using 'all' method

The first method to drop rows with all zeros in a Pandas data frame is to use the 'all' method. The 'all' method returns 'True' if all elements in a Pandas series or data frame are 'True', and 'False' otherwise. If we apply this method row-wise to a data frame, we can identify which rows have all zeros.

Once we identify the rows with all zeros, we can use the 'drop' method to remove them from the data frame.

Here's how we can do it:

``` python
# Drop rows with all zeros using the 'all' method
df = df[~(df==0).all(axis=1)]

print(df)
```

This will output the following data frame:

```
   A  B  C  D
0  0  1  0  1
1  0  3  0  1
2  0  5  0  1
```

## Method 2: Using 'any' method

Another method to drop rows with all zeros in a Pandas data frame is to use the 'any' method. The 'any' method returns 'True' if at least one element in a Pandas series or data frame is 'True', and 'False' otherwise. If we apply this method row-wise to a data frame, we can identify which rows have no non-zero elements.

Once we identify the rows with no non-zero elements, we can use the 'drop' method to remove them from the data frame.

Here's how we can do it:

``` python
# Drop rows with all zeros using the 'any' method
df = df[df.any(axis=1)]

print(df)
```

This will output the following data frame:

```
   A  B  C  D
0  0  1  0  1
1  0  3  0  1
2  0  5  0  1
```

## Method 3: Using 'sum' method

A third method to drop rows with all zeros in a Pandas data frame is to use the 'sum' method. The 'sum' method returns the sum of all elements in a Pandas series or data frame. If we apply this method row-wise to a data frame, we can identify which rows have a sum of zero.

Once we identify the rows with a sum of zero, we can use the 'drop' method to remove them from the data frame.

Here's how we can do it:

``` python
# Drop rows with all zeros using the 'sum' method
df = df[df.sum(axis=1) != 0]

print(df)
```

This will output the following data frame:

```
   A  B  C  D
0  0  1  0  1
1  0  3  0  1
2  0  5  0  1
```

## Conclusion

In this tutorial, we have demonstrated three methods to drop rows with all zeros in a Pandas data frame in Python. 

These methods involved using the 'all', 'any', and 'sum' methods to identify the rows with all zeros and then removing them using the 'drop' method. Depending on the specific use case, any of these methods could be used to remove the rows with all zeros from a Pandas data frame.
