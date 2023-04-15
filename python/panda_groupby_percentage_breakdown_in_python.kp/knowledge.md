---
title: How to use groupby in pandas to calculate the percentage of a total?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can calculate the percentage of total by group using the groupby() and transform() methods in Pandas.
---

**Contents**

[TOC]

Section 1: Introduction
Pandas is a powerful open-source data analysis library that is widely used in the domain of data science. It provides a variety of functions for data manipulation, analysis, and visualization. One of the most common tasks in data analysis is to calculate the percentage of the total for a group of items or categories. In this tutorial, we will discuss how to calculate the percentage of the total using the Pandas library in Python.

Section 2: Groupby function
The groupby function in Pandas is a powerful tool for grouping data based on one or more columns. This function returns a groupby object that can be used to apply various operations, such as sum, count, mean, etc., to the grouped data. To use the groupby function, we start by importing the Pandas library and loading the data into a Pandas DataFrame. We can then group the data using the groupby function by specifying the column(s) to group on.

Section 3: Applying functions to groups
Once we have grouped the data using the groupby function, we can apply various functions to the groups. For example, we can use the sum function to calculate the total for each group, and then divide each group by the total to calculate the percentage of the total. This can be done using the apply function in Pandas, which allows us to apply a function to each group.

Section 4: Calculation of percentage of total
To calculate the percentage of the total using the groupby function in Pandas, we can follow these steps:
1. Group the data using the groupby function by specifying the column(s) to group on
2. Apply the sum function to the grouped data to calculate the total for each group
3. Divide each group by the total to calculate the percentage of the total for each group
4. Format the output as required using the Pandas functions for formatting

Example code:

``` python
import pandas as pd

# load the data into a Pandas DataFrame
data = pd.read_csv('data.csv')

# group the data by a column
grouped_data = data.groupby('column_name')

# calculate the sum for each group
totals = grouped_data['column_to_sum'].sum()

# calculate the percentage of the total for each group
percentages = totals / totals.sum() * 100

# format the output as required
output = percentages.round(2).astype(str) + '%'

# print the output
print(output)
```

This code will group the data by a column, calculate the sum for each group, calculate the percentage of the total for each group, format the output as a percentage, and print the output.
