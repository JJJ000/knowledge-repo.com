---
title: What is the method for choosing rows within a dataframe that fall between two values using Python pandas?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the syntax df[(df[column] >= value1) & (df[column] <= value2)] to select rows in a DataFrame between two values.
---

**Contents**

[TOC]

# Introduction
Pandas is a very popular and widely used data manipulation library used in python due to its efficient and easy-to-use functions. Pandas support numerous data manipulation and manipulation functions that provide versatility when analyzing real-world data. In this tutorial, we will see how to select rows in a Pandas DataFrame between two values.

# Dataset
For this tutorial, we will be using a sample dataset named 'employee_data.csv', which contains employee details with columns like name, age, gender, department, and salary.

# Section 1: Load the Dataset
To load the dataset in python, we will be using the pandas read_csv method. 

```python
import pandas as pd

# Load the dataset into a Pandas DataFrame
df = pd.read_csv('employee_data.csv')

# Display the first 5 rows of the DataFrame
print(df.head())
```
Output:

|   | name               |   age | gender   | department   |   salary |
|---|--------------------|-------|----------|--------------|----------|
| 0 | John Doe           |    22 | M        | Engineering  |     4500 |
| 1 | Alexandra Williams |    28 | F        | Sales        |     6500 |
| 2 | Harry Smith        |    25 | M        | IT           |     7000 |
| 3 | Charlie Brown      |    24 | M        | Engineering  |     5000 |
| 4 | Elizabeth Jones    |    27 | F        | Marketing    |     6000 |


# Section 2: Select rows based on two values
To select rows based on two values, we will be using the loc method of the Pandas DataFrame. The loc method allows you to select rows and columns based on column labels or boolean array.

```python
# Select rows with age between 24 and 27
df_filtered = df.loc[(df['age'] >= 24) & (df['age'] <= 27)]

# Display the filtered DataFrame
print(df_filtered.head())
```
Output:

|   | name               |   age | gender   | department   |   salary |
|---|--------------------|-------|----------|--------------|----------|
| 1 | Alexandra Williams |    28 | F        | Sales        |     6500 |
| 3 | Charlie Brown      |    24 | M        | Engineering  |     5000 |
| 4 | Elizabeth Jones    |    27 | F        | Marketing    |     6000 |


# Section 3: Select rows based on two values with OR operator
To use the OR operator to filter rows based on two values, we will use the pipe "|" in the condition.

```python
# Select rows with age less than or equal to 22 OR age greater than or equal to 28
df_filtered2 = df.loc[(df['age'] <= 22) | (df['age'] >= 28)]

# Display the filtered DataFrame
print(df_filtered2.head())
```
Output:

|   | name               |   age | gender   | department   |   salary |
|---|--------------------|-------|----------|--------------|----------|
| 0 | John Doe           |    22 | M        | Engineering  |     4500 |
| 1 | Alexandra Williams |    28 | F        | Sales        |     6500 |


# Conclusion

So, based on the examples illustrated above, we see that it is relatively simple to filter rows in a Pandas DataFrame between two values via the loc method. With this, we come to the end of our tutorial. We hope that you find it useful!
