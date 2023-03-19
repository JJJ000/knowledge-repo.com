---
title: What are the steps to extract rows from a pandas dataframe that correspond to a specific string pattern?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the `str.contains()` method with the appropriate string pattern and apply it to the desired column of the Pandas dataframe.
---

**Contents**

[TOC]

## Introduction

Pandas is a powerful library for data manipulation in Python. One of the common tasks in data analysis is filtering rows based on a specific pattern in the data. In this tutorial, we will see how to filter rows containing a string pattern from a Pandas dataframe in Python.


## Step 1: Importing Required Libraries

To work with Pandas, we need to import it first. Additionally, we will also import Numpy and Pandas libraries.

``` python
import pandas as pd
import numpy as np
```


## Step 2: Loading Data

For the illustration in this tutorial, we will load data directly into the dataframe. In real-world problems, you will be working with data from `.csv`, `xls` or other data storing formats.

``` python
data = {'name': ['John', 'Doe', 'Mary', 'Henry', 'Jack'],
        'age': [23, 45, 18, 53, 33],
        'city': ['New York', 'Chicago', 'Los Angeles', 'Houston', 'Miami']}
df = pd.DataFrame(data)
print(df)
```

Output:
```
     name  age          city
0    John   23      New York
1     Doe   45       Chicago
2    Mary   18   Los Angeles
3   Henry   53       Houston
4    Jack   33         Miami
```


## Step 3: Filtering rows containing a pattern

We can filter rows based on string patterns using the `str.contains()` method, which returns a boolean Series indicating whether each string contains the specified pattern. To illustrate it more better, we will now filter out only those rows which contains the string _'Yor'_ from the column _'city'_ in our dataframe.

``` python
pattern = 'Yor'
filtered_df = df[df['city'].str.contains(pattern)]
print(filtered_df)
```

Output:
```
   name  age      city
0  John   23  New York
```

As you can see, we have successfully filtered out the rows containing the string pattern and got the resultant dataframe.
