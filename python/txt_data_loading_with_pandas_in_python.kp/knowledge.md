---
title: Retrieve information from a text file using pandas
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: To load data from a txt file with pandas in Python, use the pd.read\_csv() function with the appropriate file path and delimiter specified.
---

**Contents**

[TOC]

## Section 1: Introduction to the task
In data analysis and machine learning tasks, it is quite common to work with tabular data that is stored in a text file in a delimited format like CSV (comma-separated values), TSV (tab-separated values), or similar. In such cases, we can use the pandas library in Python to load, manipulate and analyze the data.

In this task, we will look at how to load data from a text file in a delimited format using pandas in Python.

## Section 2: Loading data from a CSV file
CSV (Comma-Separated Values) is a file format used for storing tabular data in plain text form where the values are separated by commas. To load data from a CSV file using pandas, we can use the `read_csv()` function. 

Here is an example of how to use the `read_csv()` function to load data from a CSV file:

```python
import pandas as pd
data = pd.read_csv('data.csv')
```

This will load the data from the file `"data.csv"` into a pandas dataframe named `data`.

By default, the `read_csv()` function assumes that the first row of the CSV file contains the column names. If the column names are not present in the file, we can use the `header=None` parameter to tell pandas to not use the first row as column names. We can also specify the delimiter character using the `delimiter` or `sep` parameter.

## Section 3: Loading data from a TSV file
TSV (Tab-Separated Values) is a file format used for storing tabular data in plain text form where the values are separated by tab characters. To load data from a TSV file using pandas, we can use the `read_csv()` function with the `delimiter='\t'` parameter.

Here is an example of how to use the `read_csv()` function to load data from a TSV file:

```python
import pandas as pd
data = pd.read_csv('data.tsv', delimiter='\t')
```

This will load the data from the file `"data.tsv"` into a pandas dataframe named `data`, where the values are separated by tabs.

## Section 4: Conclusion
In this tutorial, we saw how to use the pandas library to load data from a text file in a delimited format (CSV or TSV). We can use the `read_csv()` function to load data from a CSV file and the `delimiter='\t'` parameter to load data from a TSV file. Pandas makes it very easy to manipulate and analyze tabular data once loaded into a dataframe.
