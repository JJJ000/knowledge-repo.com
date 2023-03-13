---
title: What is the method for acquiring the overall row count in a csv file using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Read the CSV file using Python`s built-in csv module and count the number of rows using a loop or len() function.
---

**Contents**

[TOC]

## Reading the CSV file

The pandas library in Python offers an efficient way to read and manipulate CSV files. 

```python
import pandas as pd

# Read the CSV file
df = pd.read_csv('filename.csv')
```

## Obtaining the total number of rows

After reading the CSV file with pandas, we can obtain the total number of rows in the file using the `shape` attribute. The `shape` attribute is a tuple that contains the number of rows and columns in the dataframe. 

```python
# Obtain the shape of the dataframe
num_rows = df.shape[0]

# Print the number of rows in the dataframe
print(f"Number of rows: {num_rows}")
```

Alternatively, we can use the `len` function to obtain the number of rows in the dataframe.

```python
# Obtain the number of rows in the dataframe using len()
num_rows = len(df)

# Print the number of rows in the dataframe
print(f"Number of rows: {num_rows}")
```
