---
title: Locate the distinct entries within a column and subsequently arrange them in order
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the pandas library in Python to find the unique values in a column using the `unique()` method, and then use the `sort\_values()` method to sort them in ascending or descending order.
---

**Contents**

[TOC]

## Importing the Required Libraries
In order to find the unique values in a column and sort them in Python, we need to use the pandas library. Therefore, we need to import the required libraries first as shown below.

```python
import pandas as pd
```

## Creating the DataFrame

Now, we need to create a sample dataset using a dictionary object. We can use the pd.DataFrame() function to create a pandas DataFrame object with the dictionary keys as column headers and corresponding values as elements of that column.

```python
data = {'Name': ['John', 'Mary', 'Jessica', 'John', 'Bill', 'Mary'], 'Age': [23, 25, 27, 23, 30, 25], 'Gender': ['Male', 'Female', 'Female', 'Male', 'Male', 'Female']}

df = pd.DataFrame(data)
```

## Finding Unique Values in a Column and Sorting Them
Now, to find the unique values in a column, we can use the unique() method of the pandas DataFrame. Once we have found the unique values, we can use the sort() method to sort them in ascending order.

```python
unique_gender = df['Gender'].unique()
unique_gender.sort()

print(unique_gender)
```
This will return a sorted list of unique values in the 'Gender' column of the DataFrame.

```
['Female' 'Male']
```

## Conclusion
In this tutorial, we have learned how to find the unique values in a column and sort them in Python using the pandas library. We have used the unique() and sort() methods to achieve this.
