---
title: Perform a groupby operation on a pandas dataframe and choose the value that appears the most frequently
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To group a Pandas DataFrame and select the most common value, use the `groupby()` and `value\_counts()` functions, and then use `idxmax()` to get the index of the highest value.
---

**Contents**

[TOC]

# Introduction
In this tutorial, we will learn how to group a pandas DataFrame by a column and select the most common value in each group. This is a common data manipulation task that is useful when working with categorical data. We will use the pandas groupby function and the value_counts method.

# Sample Data
For this tutorial, we will use a sample data that contains information about employees in a company. The data has the following columns:

- Employee Name
- Department
- Age
- Gender
- Marital Status

```python
import pandas as pd

data = {'Employee Name': ['John', 'Mary', 'Peter', 'Jane', 'Joe', 'Anna'], 
        'Department': ['Marketing', 'Sales', 'Marketing', 'Sales', 'Sales', 'Marketing'], 
        'Age': [25, 30, 35, 40, 45, 50], 
        'Gender': ['Male', 'Female', 'Male', 'Female', 'Male', 'Female'],
        'Marital Status': ['Single', 'Married', 'Single', 'Married', 'Single', 'Married']}

df = pd.DataFrame(data)

print(df)
```

Output:

``` python
  Employee Name Department  Age  Gender Marital Status
0          John  Marketing   25    Male         Single
1          Mary     Sales   30  Female        Married
2         Peter  Marketing   35    Male         Single
3          Jane     Sales   40  Female        Married
4           Joe     Sales   45    Male         Single
5          Anna  Marketing   50  Female        Married
```

# GroupBy and Value Counts
In order to group the DataFrame by Department and select the most common gender in each group, we can use the following code:

```python
grouped_df = df.groupby('Department')['Gender'].apply(lambda x: x.mode().iat[0])

print(grouped_df)
```

Output:

```python
Department
Marketing    Female
Sales        Female
Name: Gender, dtype: object
```

The groupby function is used to group the DataFrame by the 'Department' column. The apply function is then used to apply a lambda function to each group. The lambda function calculates the mode (most common value) of the 'Gender' column using the value_counts method. The lambda function then selects the first value in the mode array (iat[0]) as the most common value. The index of the resulting DataFrame is the 'Department' column, and the values are the most common gender in each group.

# Bonus: Apply Multiple Functions
We can also apply multiple functions to each group using the agg method. For example, if we want to calculate the mean age and select the most common gender in each group, we can use the following code:

```python
grouped_df = df.groupby('Department').agg({'Age': 'mean', 'Gender': lambda x: x.mode().iat[0]})

print(grouped_df)
```

Output:

``` python
                  Age  Gender
Department                   
Marketing   36.666667  Female
Sales       38.333333  Female
```

The agg method accepts a dictionary that specifies the column name and the function to be applied to that column. In this example, we calculate the mean age of each group using the 'Age' column and calculate the most common gender using the lambda function. The resulting DataFrame has 'Department' as the index, 'Age' and 'Gender' as columns, and the mean age and most common gender in each group as values.
