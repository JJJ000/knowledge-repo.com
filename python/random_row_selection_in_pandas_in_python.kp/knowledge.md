---
title: Selecting rows in a pandas dataframe randomly
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the `df.sample()` method to randomly select rows in a Pandas dataframe.
---

**Contents**

[TOC]

## Section 1: Overview
In a Pandas dataframe, there are different methods to randomly select rows from the dataframe. This can be useful when data is too large and we only want to select a random subset of data. 

## Section 2: Using .sample() function
One method to randomly select rows from a dataframe is to use the `.sample()` function. The `.sample()` function can be used with or without replacement, depending on the data we are working with. The following is the generic syntax to use the `.sample()` function:

```
df.sample(n=None, frac=None, replace=False, weights=None, random_state=None, axis=None)
```

where

- n = number of random rows to select
- frac = fraction of random rows to select
- replace = whether to sample with replacement or not
- weights = gives a weight to each row in the dataframe, i.e., some rows are more likely to be selected than others 
- random_state = sets the seed for the random number generator
- axis = specifies whether the random rows should be selected from the rows (axis=0) or columns (axis=1)

For example, the following code selects 3 random rows from the dataframe `df`:

```python
import pandas as pd
df = pd.read_csv("data.csv")
random_rows = df.sample(n=3)
```

## Section 3: Using .iloc[ ] function
Another method to randomly select rows from a Pandas dataframe is to use the `.iloc[]` function. The `.iloc[]` function returns rows or columns by their integer position, which can be randomly shuffled to select random rows. The following code selects 3 random rows from the dataframe `df` using the `.iloc[]` function:

```python
import pandas as pd
import numpy as np
df = pd.read_csv("data.csv")
n = 3 # number of random rows to select
random_rows = df.iloc[np.random.permutation(len(df))[:n]]
```

The `np.random.permutation()` function shuffles the integer positions of the rows in the dataframe, and the `[:n]` indexing selects the first `n` shuffled positions to select the random rows.

## Section 4: Using .sample() function with weights
A final method to randomly select rows from a Pandas dataframe is to use the `.sample()` function with weights. The `.sample()` function can take a weight parameter which assigns a weight to each row in the dataframe. Rows with higher weights will be more likely to be selected than rows with lower weights. The following code selects 3 random rows from the dataframe `df` using the `.sample()` function with weights:

```python
import pandas as pd
df = pd.read_csv("data.csv")
weights = [0.1, 0.3, 0.6] # assign weights to each row
random_rows = df.sample(n=3, weights=weights)
```

In this case, rows with weight 0.6 will be chosen more often than rows with weight 0.1 because they have higher weights.
