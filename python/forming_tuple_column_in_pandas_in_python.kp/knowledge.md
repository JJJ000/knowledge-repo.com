---
title: How can a tuple column be created from two columns using pandas?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the `zip` function to combine the two columns into tuples, and assign the result to a new column in the Pandas DataFrame.
---

**Contents**

[TOC]

## Introduction
Sometimes it's useful to combine two or more columns of a dataframe into a single tuple column. This can be done using pandas' `apply` method, which can be used to apply a user-defined function to the columns of interest. In this tutorial, we will learn how to form a tuple column from two columns in pandas.

## Step 1: Importing Required Libraries and Creating a Sample DataFrame
First, we need to import the pandas library and create a sample dataframe as follows:

```python
import pandas as pd

# create a sample dataframe
df = pd.DataFrame({'col1': [1, 2, 3, 4],
                   'col2': ['a', 'b', 'c', 'd']})
```

This creates a sample dataframe with two columns, `col1` and `col2`.

## Step 2: Defining a Function to Combine Two Columns into a Tuple

Next, we define a function that takes two columns as input and returns a tuple column:

```python
def combine_columns(col1, col2):
    return list(zip(col1, col2))
```

The `zip` function is used here to combine the values in `col1` and `col2` into a tuple. The `list` function is used to convert the output of `zip` into a list.

## Step 3: Applying the Function to the DataFrame Columns
Now, we can apply the `combine_columns` function to the `col1` and `col2` columns of the dataframe using pandas' `apply` method:

```python
df['col3'] = df.apply(lambda row: combine_columns(row['col1'], row['col2']), axis=1)
```

In this example, a new column called `col3` is created in the dataframe, and the `combine_columns` function is applied to each row of the `col1` and `col2` columns using the `lambda` function. The `axis=1` argument tells `apply` to apply the function along each row of the dataframe.

## Step 4: Previewing the Modified DataFrame
Finally, we can preview the resulting dataframe using the `head` method:

```python
print(df.head())
```

This will print the first five rows of the modified dataframe, which should include the newly created `col3` column.

## Conclusion
In this tutorial, we learned how to combine two columns of a dataframe into a tuple column using pandas' `apply` method. By defining a custom function that takes two columns as input and returns a tuple column, we can apply this function to the dataframe using `apply` and create a new column that contains the combined tuples.
