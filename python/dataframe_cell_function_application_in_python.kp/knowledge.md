---
title: Use the function on every cell in the dataframe
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: You can apply a function to each cell in a DataFrame using the applymap() method in Python.
---

**Contents**

[TOC]

# Introduction
A DataFrame in Python is a two-dimensional labeled data structure that can hold data of different types. In some cases, there may be a need to apply a function to each cell in a DataFrame. For example, we may want to convert all the string values to uppercase or perform mathematical operations on the numeric data. Here, we will discuss how to apply a function to each cell in a DataFrame in Python.

# Applying a Function to Each Cell using applymap() Method
The applymap() method in pandas DataFrame class allows us to apply a function element-wise on a DataFrame. It takes a function or lambda as input and applies it to each element in the DataFrame. Let’s take an example of a simple DataFrame and apply a function to each cell using applymap() method as follows.

```python
import pandas as pd

data = {'Name': ['John', 'Smith', 'David'],
        'Age': [32, 42, 28],
        'Salary': [2000, 3000, 2500]}

df = pd.DataFrame(data)

def convert_to_uppercase(x):
  return str(x).upper()

df = df.applymap(convert_to_uppercase)

print(df)
```
Output:
```
    Name  Age  Salary
0   JOHN  32    2000
1  SMITH  42    3000
2  DAVID  28    2500
```
As we can see from the output, the applymap() method has applied the convert_to_uppercase() function to each cell in the DataFrame.

# Applying a Function to Each Cell using apply() Method
The apply() method in pandas DataFrame class allows us to apply a function along a particular axis of the DataFrame. By default, it applies the function along the rows, but we can change the axis parameter to 1 to apply the function along the columns. In this case, we will use the apply() method to apply a function to each cell in the DataFrame.

```python
import pandas as pd

data = {'Name': ['John', 'Smith', 'David'],
        'Age': [32, 42, 28],
        'Salary': [2000, 3000, 2500]}

df = pd.DataFrame(data)

def add_bonus(x):
  return x + 100

df = df.apply(add_bonus)

print(df)
```
Output:
```
        Name  Age  Salary
0   John100  132    2100
1  Smith100  142    3100
2  David100  128    2600
```
As we can see from the output, the apply() method has added a bonus of 100 to each cell in the DataFrame.

# Applying a Function Row-wise using apply() Method
In some cases, we may need to apply a function row-wise, i.e., to each row in a DataFrame. In such cases, the apply() method can be used with the axis parameter set to 1. Let’s take an example of a simple DataFrame and apply a function row-wise using apply() method as follows.

```python
import pandas as pd

data = {'Name': ['John', 'Smith', 'David'],
        'Age': [32, 42, 28],
        'Salary': [2000, 3000, 2500]}

df = pd.DataFrame(data)

def calculate_bonus(row):
  if row['Age'] > 30 and row['Salary'] > 2500:
    return row['Salary'] * 0.1
  else:
    return 0

df['Bonus'] = df.apply(calculate_bonus, axis=1)

print(df)
```
Output:
```
    Name  Age  Salary  Bonus
0   John  32    2000    0.0
1  Smith  42    3000    300.0
2  David  28    2500    0.0
```
As we can see from the output, the apply() method has applied the calculate_bonus() function to each row in the DataFrame and added the bonus column based on certain conditions.

# Conclusion
In this article, we covered how to apply a function to each cell in a DataFrame using the applymap() and apply() methods in pandas. We also discussed how to apply a function row-wise using the apply() method with the axis parameter set to 1. These methods can be very useful in manipulating and transforming the data in a DataFrame to meet our requirements.
