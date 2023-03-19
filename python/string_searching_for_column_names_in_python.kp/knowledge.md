---
title: Determine the column that includes a particular string in its name
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: The following code can be used to find the column names containing a specific string in a Pandas dataframe `df.columns[df.columns.str.contains(`specific\_string`)]`.
---

**Contents**

[TOC]

## Section 1: Introduction
In this task, we will learn how to find a column whose name contains a specific string in Python. We will be using the pandas library for this task.

## Section 2: Finding the column using pandas
We can find a column whose name contains a specific string using pandas by iterating through the column names and checking if the specified string is in the column name. Here is an example code snippet to achieve this:

```python
import pandas as pd

# read the csv file into a pandas dataframe
df = pd.read_csv('data.csv')

# iterate through the column names and check if the specified string is in the column name
for name in df.columns:
    if 'specific_string' in name:
        print(name)
```
In this code, we first read the csv file into a pandas dataframe using the `pd.read_csv()` method. We then iterate through the column names using a for loop and check if the specified string is in the current column name using an if statement. If the specified string is in the column name, we print the column name.

## Section 3: Example
Let's see an example to better understand this. Consider the following dataframe:

|index|column_one|specific_string_one|specific_string_two|
|-----|----------|------------------|------------------|
|   0 |    0     |        1         |         2        |
|   1 |    3     |        4         |         5        |
|   2 |    6     |        7         |         8        |

We want to find the column whose name contains "string_one". Using the code snippet from section 2, we get the following output:

```
specific_string_one
```

## Section 4: Conclusion
In this task, we learned how to find a column whose name contains a specific string in Python using pandas. We saw an example code snippet and a sample output. We can use this method to filter our dataframe based on column names.
