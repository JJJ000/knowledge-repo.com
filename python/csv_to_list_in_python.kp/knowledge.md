---
title: How can I convert csv to a list using python's import function?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: To import a CSV file into a list in Python, you can use the csv.reader function.
---

**Contents**

[TOC]

Section 1: Introduction
One common task in Python programming is to read data from a CSV file and store it in a list. CSV (Comma Separated Values) files are a popular format for storing tabular data in plain text, and Python provides built-in capabilities for working with them.

Section 2: Using the csv module
One popular way to import CSV data into a list is to use the built-in csv module. This module provides a reader object that can be used to iterate over the rows in a CSV file, and each row can be added to a list.

Here's an example:

```python
import csv

data_list = []

with open('data.csv') as csv_file:
    csv_reader = csv.reader(csv_file)
    for row in csv_reader:
        data_list.append(row)
```

In this example, the `csv` module is imported, and a list called `data_list` is created to hold the CSV data. The `with` statement is used to open the CSV file and create a file object called `csv_file`. A reader object is created using the `csv.reader()` method, and it is used to iterate over the rows in `csv_file`. For each row, the `append()` method is used to add it to the `data_list`.

Section 3: Using pandas
Another popular way to import CSV data into a list is to use the pandas library. Pandas is a powerful data manipulation tool for Python that provides several functions for working with CSV files.

Here's an example:

```python
import pandas as pd

data_list = pd.read_csv('data.csv').values.tolist()
```

In this example, the `pandas` library is imported using the common alias `pd`. A list called `data_list` is created by reading the CSV file using the `pd.read_csv()` function and converting the resulting DataFrame to a list using the `values.tolist()` method.

Section 4: Conclusion
Reading CSV data into a list is a common task in Python programming, and there are several ways to accomplish it. The built-in `csv` module and the pandas library are two popular options, each with their own advantages and disadvantages. By using these tools, Python developers can easily load CSV data into a list and work with it in their applications.
