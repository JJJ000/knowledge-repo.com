---
title: Using pandas, how to read an excel file in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: To read an Excel file in Python using pandas, use the pd.read\_excel() function.
---

**Contents**

[TOC]

## Introduction
Python is an open-source programming language that is widely used for data analysis and manipulation, and Pandas is a popular Python library that is used for data analysis. In this tutorial, we will learn how to read an Excel file in Python using the Pandas library.

## Installing Pandas
Before we start reading an Excel file in Python using the Pandas library, we need to make sure that we have installed the Pandas library. To install the Pandas library, open your terminal or command prompt and type the following command:

```
pip install pandas
```

## Reading an Excel file in Python using Pandas
To read an Excel file in Python using Pandas, we can use the `read_excel()` function. The `read_excel()` function reads the data from the specified Excel file into a Pandas DataFrame object. Here is an example code that reads an Excel file named 'example.xlsx':

```python
import pandas as pd

# Specify the path of the Excel file
path = "example.xlsx"

# Read the Excel file into a Pandas DataFrame
df = pd.read_excel(path)

# Print the DataFrame
print("The contents of the Excel file are:")
print(df)
```

## Specifying Sheet name
You can also specify the name of the sheet in the Excel file that you want to read. To do this, you can pass the `sheet_name` parameter to the `read_excel()` function. Here is an example code that reads the data from the sheet named 'Sheet1' in an Excel file named 'example.xlsx':

```python
import pandas as pd

# Specify the path of the Excel file
path = "example.xlsx"

# Read the sheet named 'Sheet1' into a Pandas DataFrame
df = pd.read_excel(path, sheet_name='Sheet1')

# Print the DataFrame
print("The contents of the Excel sheet are:")
print(df)
```

In this tutorial, we learned how to read an Excel file in Python using the Pandas library. We also learned how to specify the name of the sheet in the Excel file that we want to read.
