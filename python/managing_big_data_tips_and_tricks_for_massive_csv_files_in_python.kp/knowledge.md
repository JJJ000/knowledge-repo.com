---
title: Parsing an extensive .csv document
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Use the pandas library to read\_csv and store in a DataFrame.
---

**Contents**

[TOC]

# Introduction

CSV (Comma Separated Values) is a common file format used for storing tabular data. Often, CSV files can become quite massive which makes it difficult to import and analyze the data. This article outlines ways for users to read large CSV files in Python.

# Reading large CSV Files

Python provides several libraries for reading CSV files. Here are three popular methods to read large CSV files:

## Using Python's Built-in CSV library

Python's `csv` library is used to read and write data in CSV format. The `csv` library provides functions to read from CSV files iteratively, allowing it to handle large files without taking too much memory. Here's a code example:

```python
import csv

with open('large_file.csv', 'r') as file:    
    reader = csv.reader(file)
    
    for row in reader:
        print(row)
```

In the above code example, we have opened the `large_file.csv` file in read mode and then used the `csv.reader()` function to create a reader object. We have then iterated through the reader to print each row of the CSV file.

## Using Pandas library

Pandas is a popular data manipulation library in Python. It provides various functions for working with CSV files, including reading and writing. Here's an example code for reading a large CSV file using pandas:

```python
import pandas as pd

chunk_size = 1000000
for chunk in pd.read_csv("large_file.csv", chunksize=chunk_size):
    print(chunk)
```

In the above code example, we are using Pandas' `pd.read_csv()` method to read the CSV file in chunks, iterating through each chunk and printing it. The `chunksize` parameter specifies the number of rows to read for each chunk. This method is memory efficient and allows for the processing of large files without memory errors.

## Using Dask library

Dask is another library for parallel computing in Python that can handle large datasets. Dask provides a dataframe object similar to Pandas, which allows you to perform operations on large CSV files. Here's an example code for reading a large CSV file using Dask:

```python
import dask.dataframe as dd

df = dd.read_csv('large_file.csv', blocksize=None)
print(df.compute())
```

In the above code example, we are using Dask's `dd.read_csv()` method to read the CSV file. The `blocksize` parameter specifies the chunk size of the data, with `None` indicating that Dask should determine the optimal block size. The `compute()` method is used to trigger the computation of the data, allowing you to work with it as though it were in memory.

# Conclusion

In this article, we have discussed various ways to read large CSV files in Python. The `csv` library can be used for iterating through large files, while Pandas and Dask libraries offer more advanced functionality for working with a dataset. Ultimately, the choice of library will depend on the specific needs and requirements of the project at hand.
