---
title: How to show all columns of a dataframe in jupyter Python notebook?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Set the Pandas option to display all columns using `pd.set\_option(`display.max\_columns`, None)` in the notebook or script.
---

**Contents**

[TOC]

# Introduction
In this article, we will discuss how to display all columns of a dataframe in a Jupyter Python Notebook.

# Problem Statement
By default, pandas will only display a subset of columns in a dataframe. This can be a problem when working with large datasets, or when trying to compare multiple columns at once. To address this issue, we can adjust the pandas settings to display all columns in the dataframe.

# Solution
One solution is to adjust the pandas display options using the set_option() function. Specifically, we can use set_option('display.max_columns', None) to display all columns of a dataframe. 

Another solution is to simply print the dataframe, which will automatically display all columns.

# Example Code
Let's first create a sample dataframe to work with:

```
import pandas as pd

df = pd.DataFrame({
    'A': [1, 2, 3],
    'B': [4, 5, 6],
    'C': [7, 8, 9],
    'D': [10, 11, 12]
})
```

To display all columns of the dataframe, we can use the set_option() function as follows:

``` 
pd.set_option('display.max_columns', None)
print(df)
```

Alternatively, we can simply print the dataframe:

```
print(df)
```

Both of these approaches will display all columns of the dataframe:

```
   A  B  C   D
0  1  4  7  10
1  2  5  8  11
2  3  6  9  12
```
