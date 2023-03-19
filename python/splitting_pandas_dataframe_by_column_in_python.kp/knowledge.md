---
title: The dataframe of pandas can be divided based on the values present in a particular column
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: Use groupby() method with the column as parameter to split a DataFrame by column value in Pandas.
---

**Contents**

[TOC]

## Introduction
Pandas is a powerful library in Python that provides data structure for data analysis. Its DataFrame is the most commonly used data structure, which is a two-dimensional table that consists of data with labeled rows and columns. In this article, we will learn how to split a DataFrame by column value in Python using Pandas.

## Example DataFrame
Let's first create an example DataFrame that we can use to demonstrate how to split it by column value in Python using Pandas.

```python
import pandas as pd

df = pd.DataFrame({
    'Name': ['Alice', 'Bob', 'Charlie', 'David', 'Emily'],
    'City': ['Boston', 'New York', 'Chicago', 'San Francisco', 'Boston'],
    'Salary': [60000, 55000, 70000, 80000, 50000]
})

print(df)
```

```
       Name           City  Salary
0     Alice         Boston   60000
1       Bob       New York   55000
2   Charlie        Chicago   70000
3     David  San Francisco   80000
4     Emily         Boston   50000
```

This DataFrame has three columns: `Name`, `City`, and `Salary`.

## Split DataFrame by Unique Column Values

To split a DataFrame by unique column values, we can use the `groupby` method in Pandas. This method groups the DataFrame by a specified column and returns a groupby object, which can be iterated over to access each group.

```python
groups = df.groupby('City')

for name, group in groups:
    print('City:', name)
    print(group)
    print()
```

This code splits the DataFrame `df` by the unique values in the `City` column and iterates over each group. For each group, it prints the city name and the corresponding rows in the DataFrame.

```
City: Boston
    Name    City  Salary
0  Alice  Boston   60000
4  Emily  Boston   50000

City: Chicago
      Name     City  Salary
2  Charlie  Chicago   70000

City: New York
  Name      City  Salary
1  Bob  New York   55000

City: San Francisco
    Name           City  Salary
3  David  San Francisco   80000
```

## Split DataFrame by Multiple Column Values

To split a DataFrame by multiple column values, we can pass a list of column names to the `groupby` method.

```python
groups = df.groupby(['City', 'Salary'])

for name, group in groups:
    print('City, Salary:', name)
    print(group)
    print()
```

This code splits the DataFrame `df` by the unique combinations of values in the `City` and `Salary` columns and iterates over each group. For each group, it prints the city and salary values and the corresponding rows in the DataFrame.

```
City, Salary: ('Boston', 50000)
    Name    City  Salary
4  Emily  Boston   50000

City, Salary: ('Boston', 60000)
    Name    City  Salary
0  Alice  Boston   60000

City, Salary: ('Chicago', 70000)
      Name     City  Salary
2  Charlie  Chicago   70000

City, Salary: ('New York', 55000)
  Name      City  Salary
1  Bob  New York   55000

City, Salary: ('San Francisco', 80000)
    Name           City  Salary
3  David  San Francisco   80000
```

## Split DataFrame by Column Value

To split a DataFrame by a specific column value, we can use boolean indexing to create a new DataFrame that contains only the rows with the specified value.

```python
df_boston = df[df['City'] == 'Boston']

print(df_boston)
```

This code creates a new DataFrame `df_boston` that contains only the rows where the `City` column is equal to `'Boston'`.

```
    Name    City  Salary
0  Alice  Boston   60000
4  Emily  Boston   50000
```

## Conclusion
In this article, we have learned how to split a DataFrame by column value in Python using Pandas. We can split a DataFrame by unique column values, multiple column values, or a specific column value using the `groupby` method, boolean indexing, or a combination of both.
