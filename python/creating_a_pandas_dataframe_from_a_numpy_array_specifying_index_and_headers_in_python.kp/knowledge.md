---
title: How can I assign an index column and column headers when constructing a pandas dataframe from a numpy array?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: You can specify the index column and column headers when creating the DataFrame by passing the index and column names as arguments to the DataFrame constructor.
---

**Contents**

[TOC]

**Creating a Pandas DataFrame**

A DataFrame is a two-dimensional data structure that contains rows and columns. It can be created from a variety of data sources, including a Numpy array. To create a Pandas DataFrame from a Numpy array, we can use the `pd.DataFrame()` function. 

**Specifying the Index Column**

The `pd.DataFrame()` function takes a parameter called `index`, which can be used to specify the index column. This parameter can be a list of labels, a NumPy array, or a Pandas Index. For example, if we have a Numpy array called `data` and we want to use the first column as the index column, we can do the following:

```python
import pandas as pd

data = np.array([[1, 2, 3],
                 [4, 5, 6],
                 [7, 8, 9]])

df = pd.DataFrame(data, index=data[:, 0])
```

**Specifying the Column Headers**

The `pd.DataFrame()` function also takes a parameter called `columns`, which can be used to specify the column headers. This parameter can be a list of labels or a NumPy array. For example, if we have a Numpy array called `data` and we want to use the first row as the column headers, we can do the following:

```python
import pandas as pd

data = np.array([[1, 2, 3],
                 [4, 5, 6],
                 [7, 8, 9]])

df = pd.DataFrame(data, columns=data[0, :])
```
