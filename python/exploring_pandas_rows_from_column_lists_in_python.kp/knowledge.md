---
title: For every element in a list within a pandas column, generate a new row
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the explode() function on the column of lists to create a separate row for each element in the list.
---

**Contents**

[TOC]

## Introduction

Pandas is an extremely popular Python data manipulation library that provides easy-to-use data structures for efficiently analyzing structured/tabular data. One of the data structures provided by Pandas is DataFrame, which is comprised of rows and columns (similar to a spreadsheet). It's quite common to have a column of lists within a DataFrame, and in some cases, we may want to create a new row for each list element. In this tutorial, we'll walk through how to achieve this in Pandas.


## Creating a pandas dataframe with a column of lists

Before we start creating new rows for each list element, let's first create a sample DataFrame that includes a column of lists. We'll use the pandas.DataFrame() constructor to create a new DataFrame, and pass in a dictionary containing key-value pairs for each column in the DataFrame. For our purposes, we'll include a single column called 'list_col', which will contain a variable number of lists.

Here's the code:

```python
import pandas as pd

# create sample data
data = {'list_col': [[1,2,3], [4,5], [6,7,8,9], [10]]}

# create pandas dataframe
df = pd.DataFrame(data)

# show the dataframe
print(df)
```

This will output:

```
        list_col
0     [1, 2, 3]
1        [4, 5]
2  [6, 7, 8, 9]
3           [10]
```


## Creating new rows for each list element

Now that we have a DataFrame with a column of lists, we can create a new row for each list element. To do this, we'll use the pandas.DataFrame.explode() method, which creates a new row for each element in a specified column.

Here's the code:

```python
# explode the list_col column into new rows
df_exploded = df.explode('list_col')

# show the exploded dataframe
print(df_exploded)
```

This will output:

```
  list_col
0        1
0        2
0        3
1        4
1        5
2        6
2        7
2        8
2        9
3       10
```


## Resetting the DataFrame index

If we look closely at the output of the previous code block, we'll see that the row index is not sequential any more. This is because the pandas.DataFrame.explode() method maintains the original index of the DataFrame. In most cases, this is not ideal, and we'll want to reset the index to be sequential. We can do this using the pandas.DataFrame.reset_index() method.

Here's the updated code:

```python
# explode the list_col column into new rows
df_exploded = df.explode('list_col')

# reset the index
df_exploded = df_exploded.reset_index(drop=True)

# show the exploded dataframe with reset index
print(df_exploded)
```

This will output:

```
  list_col
0        1
1        2
2        3
3        4
4        5
5        6
6        7
7        8
8        9
9       10
```


## Conclusion

In this tutorial, we demonstrated how to create new rows for each element in a column of lists in a Pandas DataFrame. Specifically, we used the pandas.DataFrame.explode() method to do this, and also reset the index to be sequential using the pandas.DataFrame.reset_index() method. This technique can be very useful for working with structured data that contains nested lists.
