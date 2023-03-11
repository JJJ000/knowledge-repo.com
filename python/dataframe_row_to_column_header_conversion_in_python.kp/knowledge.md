---
title: Change the row data into column headers for a pandas dataframe
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: To convert a row to a column header for a Pandas DataFrame in Python, use the transpose method df = df.transpose() (or df.T).
---

**Contents**

[TOC]

# Introduction

Pandas is a popular data manipulation library for Python. It provides a way to work with data in various formats such as CSV, Excel, SQL databases, or web scraping. Pandas DataFrame is one of the most commonly used data structures. By default, a DataFrame has rows and columns, but sometimes we may need to convert a row to header or vice versa. In this tutorial, we will discuss how to convert a row to a column header for Pandas DataFrame in Python.

# Sample Data

Let's create some sample data to demonstrate the conversion of a row to a column header.

```python
import pandas as pd

data = {'Name': ['Alice', 'Bob', 'Charlie'], 
        'Q1': [80, 70, 90], 
        'Q2': [85, 75, 95],
        'Q3': [90, 80, 85]}

df = pd.DataFrame(data)
print(df)
```

Output:

```
       Name  Q1  Q2  Q3
0     Alice  80  85  90
1       Bob  70  75  80
2  Charlie   90  95  85
```

# Using the set_index() Method

The simplest way to convert a row to a column header is to set the index of the DataFrame to that row using the set_index() method.

```python
df = df.set_index('Name')
print(df)
```

Output:

```
         Q1  Q2  Q3
Name              
Alice    80  85  90
Bob      70  75  80
Charlie  90  95  85
```

In this example, we set the index to the 'Name' column, which converted that row to column headers.

# Transposing the DataFrame

Another way to convert a row to a column header is to transpose the DataFrame using the T attribute. This method simply switches the rows and columns.

```python
df = df.T
print(df)
```

Output:

```
Name  Alice  Bob  Charlie
Q1       80   70       90
Q2       85   75       95
Q3       90   80       85
```

In this example, we transposed the DataFrame, which converted the row to column headers.

# Using the rename() Method

We can also use the rename() method to convert a row to a column header. This method renames the row to the desired column header.

```python
df = df.rename(index={'Name': ''})
print(df)
```

Output:

```
        Alice  Bob  Charlie
Q1         80   70       90
Q2         85   75       95
Q3         90   80       85
```

In this example, we rename the 'Name' row to an empty string, which converts it to a column header.

# Conclusion

In this tutorial, we discussed three ways to convert a row to a column header for Pandas DataFrame in Python: using the set_index() method, transposing the DataFrame, and using the rename() method. These methods are simple and effective for reorganizing data as needed.
