---
title: A streamlined approach for implementing various filters on pandas dataframe or series
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Chained filtering is the most efficient way to apply multiple filters to a pandas DataFrame or Series in Python.
---

**Contents**

[TOC]

## Introduction

Pandas is a popular library for data analysis and manipulation in Python. One of the common tasks in data analysis is filtering data based on certain conditions. In this article, we will explore multiple ways to efficiently apply filters to pandas DataFrame or Series in Python.

## Creating the DataFrame

Before we move on to filtering the data, let us create a sample DataFrame that we can use to demonstrate the different techniques.

``` python
import pandas as pd

data = {
    'name': ['Alice', 'Bob', 'Charlie', 'David', 'Emily'],
    'age': [25, 32, 18, 47, 22],
    'gender': ['F', 'M', 'M', 'M', 'F'],
    'score': [80, 65, 90, 75, 85]
}

df = pd.DataFrame(data)
```

The DataFrame `df` contains information about the name, age, gender, and score of 5 individuals.

```
# Output
       name  age gender  score
0     Alice   25      F     80
1       Bob   32      M     65
2  Charlie   18      M     90
3     David   47      M     75
4     Emily   22      F     85
```

## Method 1: Using Boolean indexing

The most common and efficient way to filter data in pandas is by using Boolean indexing.

Boolean indexing is a technique that allows us to select rows from a DataFrame based on a condition or multiple conditions. We can use the comparison operators (`<`, `>`, `<=`, `>=`, `==`, `!=`) to create a boolean mask that can be used to filter the data.

The basic syntax for boolean indexing is as follows:

``` python
df[condition]
```

where `df` is the DataFrame, and `condition` is the boolean mask that evaluates to `True` or `False` for each row in the DataFrame.

For example, to filter the rows where the `score` is greater than `80`, we can use the following code:

``` python
df[df['score'] > 80]
```

This will return the following output:

```
# Output
     name  age gender  score
2  Charlie   18      M     90
4    Emily   22      F     85
```

To apply multiple filters, we can use the `&` (and) and `|` (or) operators to combine the conditions.

For example, to filter the rows where the `score` is greater than `80` and the `gender` is `'F'`, we can use the following code:

``` python
df[(df['score'] > 80) & (df['gender'] == 'F')]
```

This will return the following output:

```
# Output
   name  age gender  score
4  Emily   22      F     85
```

## Method 2: Using query()

Another way to filter data in pandas is by using the `query()` method.

The `query()` method allows us to filter a DataFrame using a string expression that contains the conditions we want to apply.

The basic syntax for using `query()` is as follows:

``` python
df.query('condition')
```

where `df` is the DataFrame, and `condition` is a string expression that contains the conditions we want to apply.

For example, to filter the rows where the `score` is greater than `80`, we can use the following code:

``` python
df.query('score > 80')
```

This will return the following output:

```
# Output
     name  age gender  score
2  Charlie   18      M     90
4    Emily   22      F     85
```

To apply multiple filters, we can use the `and` and `or` keywords in the string expression.

For example, to filter the rows where the `score` is greater than `80` and the `gender` is `'F'`, we can use the following code:

``` python
df.query('score > 80 and gender == "F"')
```

This will return the following output:

```
# Output
   name  age gender  score
4  Emily   22      F     85
```

## Method 3: Using loc[]

`loc[]` is another popular method for filtering data in pandas.

`loc[]` is a label-based indexer that allows us to select rows and columns from a DataFrame by label or boolean mask.

The basic syntax for using `loc[]` is as follows:

``` python
df.loc[condition]
```

where `df` is the DataFrame, and `condition` is the boolean mask or label that we want to select.

For example, to filter the rows where the `score` is greater than `80`, we can use the following code:

``` python
df.loc[df['score'] > 80]
```

This will return the following output:

```
# Output
     name  age gender  score
2  Charlie   18      M     90
4    Emily   22      F     85
```

To apply multiple filters, we can use the `&` (and) and `|` (or) operators to combine the conditions.

For example, to filter the rows where the `score` is greater than `80` and the `gender` is `'F'`, we can use the following code:

``` python
df.loc[(df['score'] > 80) & (df['gender'] == 'F')]
```

This will return the following output:

```
# Output
   name  age gender  score
4  Emily   22      F     85
```

## Conclusion

In this article, we have explored multiple ways to efficiently apply filters to pandas DataFrame or Series in Python. We have learned how to use Boolean indexing, `query()`, and `loc[]` to filter data based on one or multiple conditions. Depending on the use case and personal preference, one method might be more suitable than the others.
