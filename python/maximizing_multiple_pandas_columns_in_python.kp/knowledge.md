---
title: Discover the maximum value among two or more columns using pandas
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the `max()` function with the `axis` parameter set to 1 to find the maximum of two or more columns in Pandas, where the `axis` parameter specifies the axis to apply the function on, and `1` stands for column-wise.
---

**Contents**

[TOC]

Introduction
---
Pandas is a powerful data manipulation and analysis library for Python. In this article, we will discuss how to find the maximum value of two or more columns in a DataFrame using Pandas.

Step 1: Creating a Sample DataFrame
---
To demonstrate how to find the max of two or more columns with Pandas, we first need to create a sample DataFrame. We can create a DataFrame using the `DataFrame` function from the Pandas library.

```python
import pandas as pd 
  
# Creating sample dataframe 
data = {'name': ['John', 'Paul', 'George', 'Ringo'], 
        'age': [20, 23, 21, 22], 
        'score1': [99, 95, 75, 85], 
        'score2': [80, 92, 85, 78]} 
  
df = pd.DataFrame(data) 
```

Step 2: Finding the Maximum Value of Two Columns
---
To find the maximum value of two columns in a DataFrame, we can use the `max()` function from Pandas. We can specify the column names as a list to the `max()` function.

```python
# Finding the maximum value of two columns 
max_value = df[['score1', 'score2']].max(axis = 1) 

print(max_value)
```

In the above code, we first specified the column names from which we want to find the maximum value as a list `['score1', 'score2']` and passed it to the `max()` function. We also specified the `axis` parameter as `1` which indicates that we want to get the maximum value row-wise.

Step 3: Finding the Maximum Value of More Than Two Columns
---
To find the maximum value of more than two columns in a DataFrame, we can use the `max()` function in a similar way as in Step 2. We need to specify all the column names from which we want to find the maximum value as a list.

```python
# Finding the maximum value of more than two columns 
max_value = df[['score1', 'score2', 'age']].max(axis = 1) 

print(max_value)
```

In the above code, we specified three columns `['score1', 'score2', 'age']` from which we want to find the maximum value and passed it to the `max()` function. Again, we specified the `axis` parameter as `1` which indicates that we want to get the maximum value row-wise.

Conclusion
---
In this article, we discussed how to find the maximum value of two or more columns in a DataFrame using Pandas in Python. We used the `max()` function from the Pandas library, and specified the column names from which we want to find the maximum value as a list. We also specified the `axis` parameter to indicate whether we want to get the maximum value row-wise or column-wise.
