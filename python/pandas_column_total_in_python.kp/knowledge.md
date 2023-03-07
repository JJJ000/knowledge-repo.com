---
title: Obtain the sum of a column in a pandas data frame
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use the sum() method on the desired column of a Pandas DataFrame to get the total of that column in Python.
---

**Contents**

[TOC]

## Section 1: Introduction to Pandas
Pandas is a very popular open-source Python library used for data manipulation, data analysis, and data visualization. It offers powerful data structures for working with structured data, such as data frames and series, that make it easy to manipulate, transform, and analyze data.

## Section 2: Loading data into a DataFrame
Before we can get the total of a Pandas column, we need to first load our data into a Pandas DataFrame. A DataFrame is a two-dimensional table of data that consists of rows and columns.

We can load data into a DataFrame from various sources such as CSV, Excel, SQL database or by loading a dictionary or a list of lists directly. For the purpose of this example, we'll read a CSV file and load it into a DataFrame.

```
import pandas as pd

# Load data from CSV file into a DataFrame
df = pd.read_csv('data.csv')
```

## Section 3: Getting the total of a Pandas column
Once we have our data loaded into a DataFrame, we can easily get the total of a column by using the `sum()` method of the DataFrame. The `sum()` method returns the sum of all the values in the specified column.

Let's say our DataFrame has a column called "price" and we want to get the total of all the prices in that column:

```
import pandas as pd

# Load data from CSV file into a DataFrame
df = pd.read_csv('data.csv')

# Get the total of the "price" column
total_price = df['price'].sum()

print(f'Total price: {total_price}')
```

## Section 4: Conclusion
In conclusion, getting the total of a Pandas column is very easy. We just need to load our data into a DataFrame and use the `sum()` method of the DataFrame to get the total of the desired column. Pandas is a powerful library that makes data manipulation, analysis, and visualization easy and intuitive.
