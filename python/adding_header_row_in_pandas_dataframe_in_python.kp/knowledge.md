---
title: What is the process of including a header row in a pandas dataframe?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Use the `columns` attribute and assign it to a list of column names. 

Example 

`df.columns = [`col1`, `col2`, `col3`]`
---

**Contents**

[TOC]

## Introduction

Pandas is a popular data manipulation library in Python. Dataframes in pandas are often used to store and manipulate tabular data. When working with dataframes, it is often necessary to add a header row to the dataframe. In this tutorial, we will explore how to add a header row to a pandas dataframe in Python.

## Creating a dataframe without a header row

Before we can explore how to add a header row to a pandas dataframe, we need to create a dataframe without a header row. We can create a dataframe using the `pd.DataFrame()` constructor, passing in a list of lists as the data argument. Each inner list will be a row in the dataframe. Here's an example:

```
import pandas as pd

data = [[1, "John", 23],
        [2, "Jane", 27],
        [3, "Mary", 19]]

df = pd.DataFrame(data)
print(df)
```

This will output:

```
   0     1   2
0  1  John  23
1  2  Jane  27
2  3  Mary  19
```

Note that the dataframe doesn't have a header row. The columns are named with integers starting from zero.

## Creating a dataframe with a header row

To create a dataframe with a header row, we need to pass in a list of column names as an additional argument to the `pd.DataFrame()` constructor. Here's an example:

```
import pandas as pd

data = [[1, "John", 23],
        [2, "Jane", 27],
        [3, "Mary", 19]]

column_names = ["ID", "Name", "Age"]

df = pd.DataFrame(data, columns=column_names)
print(df)
```

This will output:

```
   ID  Name  Age
0   1  John   23
1   2  Jane   27
2   3  Mary   19
```

Note that the dataframe now has a header row with the column names "ID", "Name", and "Age".

## Adding a header row to an existing dataframe

If you already have a dataframe without a header row and you want to add a header row to it, you can do so using the `DataFrame.columns` attribute. Here's an example:

```
import pandas as pd

data = [[1, "John", 23],
        [2, "Jane", 27],
        [3, "Mary", 19]]

df = pd.DataFrame(data)

column_names = ["ID", "Name", "Age"]
df.columns = column_names

print(df)
```

This will output the same result as before:

```
   ID  Name  Age
0   1  John   23
1   2  Jane   27
2   3  Mary   19
```

Note that after assigning the list of column names to the `DataFrame.columns` attribute, the dataframe now has a header row with the column names "ID", "Name", and "Age".
