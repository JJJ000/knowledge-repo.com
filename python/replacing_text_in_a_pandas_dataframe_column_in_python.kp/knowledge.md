---
title: What is the method for substituting text in a pandas dataframe's string column?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: The `.str.replace()` method can be used to replace text in a string column of a Pandas dataframe in Python.
---

**Contents**

[TOC]

# Introduction

Pandas is one of the most widely used data manipulation libraries in Python. In Pandas, a Dataframe is a two-dimensional table with rows and columns, similar to a SQL table or an Excel spreadsheet. In this notebook, we will focus on how to replace text in a string column of a Pandas Dataframe using Pandas built-in functions.

# Package Installation

Before we proceed with the examples, we have to ensure that Pandas package is installed. If not, we'll install the package by running the following code on the command prompt or terminal:

```python
!pip install pandas
```

# Method 1: Using str.replace() function

The simplest way to replace text in a string column of a Pandas Dataframe is to use the `str.replace()` function. This function replaces all occurrences of a string with another string.

The syntax of the `str.replace()` function is as follows:

```python
dataframe['column_name'] = dataframe['column_name'].str.replace('old_string', 'new_string')
```

Let's see an example to understand this function better.

```python
import pandas as pd

# Create a dataframe
data = {'name': ['John Doe', 'Jane Doe', 'Joe Bloggs', 'Jake Smith'],
        'age': [25, 30, 35, 40],
        'city': ['New York', 'Toronto', 'Sydney', 'Dubai']}
df = pd.DataFrame(data)

# Replace 'Doe' with 'Smith' in the 'name' column
df['name'] = df['name'].str.replace('Doe', 'Smith')

# Print the updated dataframe
print(df)
```

Output:
```
         name  age      city
0  John Smith   25  New York
1  Jane Smith   30   Toronto
2  Joe Bloggs  35    Sydney
3  Jake Smith  40     Dubai
```

As we can see in the output, all occurrences of the string 'Doe' in the 'name' column have been replaced with the string 'Smith'. 

# Method 2: Using .apply() function with lambda function

Another way to replace text in a string column of a Pandas Dataframe is to use the `.apply()` function with a lambda function that applies the string replace function to each entry in the column.

The syntax of this method is as follows:

```python
dataframe['column_name'] = dataframe['column_name'].apply(lambda x: x.replace('old_string', 'new_string'))
```

Let's see an example to understand this function better.

```python
import pandas as pd

# Create a dataframe
data = {'name': ['John Doe', 'Jane Doe', 'Joe Bloggs', 'Jake Smith'],
        'age': [25, 30, 35, 40],
        'city': ['New York', 'Toronto', 'Sydney', 'Dubai']}
df = pd.DataFrame(data)

# Replace 'Doe' with 'Smith' in the 'name' column
df['name'] = df['name'].apply(lambda x: x.replace('Doe', 'Smith'))

# Print the updated dataframe
print(df)
```

Output:
```
         name  age      city
0  John Smith   25  New York
1  Jane Smith   30   Toronto
2  Joe Bloggs  35    Sydney
3  Jake Smith  40     Dubai
```

As we can see in the output, all occurrences of the string 'Doe' in the 'name' column have been replaced with the string 'Smith' using `.apply()` with a lambda function.

# Conclusion

In this notebook, we have learned two ways to replace text in a string column of a Pandas Dataframe. These methods are:

1. Using `str.replace()` function
2. Using `.apply()` function with a lambda function 

We hope this notebook will help you in your data analysis projects. Happy coding!
