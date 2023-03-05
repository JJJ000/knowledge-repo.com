---
title: What are the means to identify if a value is present in a pandas column?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Use the `.isin()` method to check if a Pandas column contains a particular value or a list of values.
---

**Contents**

[TOC]

## Introduction

Pandas is a powerful data analysis library in Python that provides efficient and effective tools for manipulating large amounts of data. One common task in data analysis is to determine whether a pandas column contains a particular value. In this article, we will explore some ways to achieve this task in Python.

## Data Preparation

Before we can check if a pandas column contains a particular value, we need to first create a pandas DataFrame that contains the column of interest. For the purpose of this tutorial, we will use the following DataFrame:

``` python
import pandas as pd

data = {'name': ['John', 'Bob', 'Alice', 'Nick', 'Lisa', 'Tom'],
        'age': [23, 45, 32, 28, 39, 41],
        'gender': ['M', 'M', 'F', 'M', 'F', 'M'],
        'country': ['USA', 'Canada', 'UK', 'Australia', 'USA', 'UK']}

df = pd.DataFrame(data)
``` 

Our goal is to determine whether the dataframe column `country` contains the value `USA`. We will now explore different ways to achieve this goal.

## Method 1: Using the `in` Operator

One simple way to check if a pandas column contains a particular value is to use the `in` operator with a Boolean indexing. Here's how it works:

``` python
if 'USA' in df['country'].values:
    print('The column contains the value "USA"')
else:
    print('The column does not contain the value "USA"')
```

This code checks if the string 'USA' is present in the values of the `country` column. If it is present, it prints a message indicating that the column contains the value 'USA'. Otherwise, it prints a message indicating that the column does not contain the value 'USA'.

## Method 2: Using the `isin()` Function

Another way to achieve the same goal is to use the `isin()` function in combination with Boolean indexing. Here's how it works:

``` python
if df['country'].isin(['USA']).any():
    print('The column contains the value "USA"')
else:
    print('The column does not contain the value "USA"')
```

In this code, the `isin()` function is used to create a Boolean index of the rows that contain the value 'USA'. The `any()` function is then used to check if any of the rows in the Boolean index are `True`, indicating that the column contains the value 'USA'. If the `any()` function returns `True`, the code prints a message indicating that the column contains the value 'USA'. Otherwise, it prints a message indicating that the column does not contain the value 'USA'.

## Conclusion

In this tutorial, we have explored two ways to check if a pandas column contains a particular value. Both methods involve using Boolean indexing and checking for the presence of `True` values. These techniques can be helpful when analyzing large amounts of data and searching for specific values or patterns.
