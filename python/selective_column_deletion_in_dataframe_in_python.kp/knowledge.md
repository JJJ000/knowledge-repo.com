---
title: What is the method to exclude certain columns and delete all other columns in a dataframe?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-15 00:00:00
updated_at: 2023-03-15 00:00:00
tldr: Use the DataFrame`s `drop` method with the argument `columns` set to a list of column names to drop all columns except for the ones listed.
---

**Contents**

[TOC]

## Introduction

A DataFrame is a 2-dimensional labeled data structure with columns of potentially different types. You might have a DataFrame that contains many columns, but only a few of them are relevant to your analysis. In such cases, deleting all the irrelevant columns manually can be a tedious task. You can use pandas to select and filter the columns you want to keep and delete the rest in one step.

## Prerequisites

To follow along with this tutorial, you should have pandas installed. You can install pandas through pip, conda or any other package manager of your choice. You should also be familiar with basic pandas operations, such as creating DataFrames, selecting columns, and filtering rows.

## Example DataFrame

To demonstrate how to remove columns from a pandas DataFrame, we'll create a sample DataFrame:

```
import pandas as pd

data = {'name': ['Alice', 'Bob', 'Charlie', 'David'],
        'age': [25, 30, 35, 40],
        'gender': ['F', 'M', 'M', 'M'],
        'salary': [50000, 60000, 70000, 80000]}

df = pd.DataFrame(data)

print(df)
```

Output:

|    | name     |   age | gender   |   salary |
|---:|:---------|------:|:---------|---------:|
|  0 | Alice    |    25 | F        |    50000 |
|  1 | Bob      |    30 | M        |    60000 |
|  2 | Charlie  |    35 | M        |    70000 |
|  3 | David    |    40 | M        |    80000 |

This DataFrame contains four columns: 'name', 'age', 'gender', and 'salary'. Let's assume that we want to keep only the 'name' and 'age' columns and delete the rest.

## Remove columns using drop()

The drop() method in pandas allows us to remove columns by specifying their names. We can use the method to drop all the columns we don't need at once. Here's the code:

```
cols_to_keep = ['name', 'age']

df = df[cols_to_keep]

print(df)
```

Output:

|    | name     |   age |
|---:|:---------|------:|
|  0 | Alice    |    25 |
|  1 | Bob      |    30 |
|  2 | Charlie  |    35 |
|  3 | David    |    40 |

Note that we used square brackets to select only specific columns. The drop() method can also be used in a similar way, but it requires more lines of code.

## Remove columns using iloc and drop()

If you want to delete columns by their numeric index rather than by name, you can combine the iloc[] method and the drop() method. Here's the code:

```
df = df.drop(df.columns[[2, 3]], axis=1)

print(df)
```

Output:

|    | name     |   age |
|---:|:---------|------:|
|  0 | Alice    |    25 |
|  1 | Bob      |    30 |
|  2 | Charlie  |    35 |
|  3 | David    |    40 |

In this example, we selected the columns to be removed by their position. We used the drop() method to delete them and passed axis=1 to specify that we want to delete columns (as opposed to rows).

## Remove columns using loc and drop()

If you want to delete columns based on some condition, you can use loc[] instead of iloc[] to select the columns and then use drop() to delete them. Here's the code:

```
df = df.drop(df.loc[:, 'gender':'salary'], axis=1)

print(df)
```

Output:

|    | name     |   age |
|---:|:---------|------:|
|  0 | Alice    |    25 |
|  1 | Bob      |    30 |
|  2 | Charlie  |    35 |
|  3 | David    |    40 |

In this example, we used loc[] to select the columns from 'gender' to 'salary'. We passed axis=1 to drop() to specify that we want to delete columns.
