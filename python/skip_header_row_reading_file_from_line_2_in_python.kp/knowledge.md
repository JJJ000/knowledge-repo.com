---
title: Retrieve data starting from line 2, excluding the header row
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Use the parameter `skiprows=1` when read\_csv or read\_table to skip the header row in a file when reading it in Python.
---

**Contents**

[TOC]

# Section 1: Introduction

When working with data files, it is common for the first row to be a header row that contains column names or variable names. However, when reading the data into Python, we may want to skip the header row and start reading the data from the second row.

In this guide, we will explore different methods to read a file from line 2 or skip header row in Python.


# Section 2: Using readline() and for loop to skip the first line

One simple way to skip the header row is to use the `readline()` method to read the first line and then use a for loop to read the remaining lines starting from the second line. Here's how you can do it:

```python
with open('data.csv', 'r') as file:
    header = file.readline()
    for line in file:
        # process the line here
        print(line.strip().split(','))
```

In this code snippet, `header` variable contains the first line of the file. The `for` loop reads the remaining lines starting from the second line and processes each line as needed.

However, this method has a couple of limitations. First, it assumes that the file has at least two rows. If the file has only one row, this method will skip that row. Second, it assumes that the header row is the first line in the file. If the header row is not the first line, this method will still read the first line and skip the header row.


# Section 3: Using itertools.islice to skip the first line

Another way to skip the header row is to use the `islice()` function from the `itertools` module. Here's how you can do it:

```python
import itertools

with open('data.csv', 'r') as file:
    header = next(file)
    for line in itertools.islice(file, 0, None):
        # process the line here
        print(line.strip().split(','))
```

In this code snippet, `header` variable contains the first line of the file. The `itertools.islice()` function reads the remaining lines starting from the second line and processes each line as needed.

Unlike the previous method, this method does not have the limitations of assuming that the file has at least two rows or that the header row is the first line in the file. The `next()` function is used to read the first line of the file and then `itertools.islice()` is used to skip that line and read the remaining lines.


# Section 4: Using pandas to read file from line 2

If you're working with a CSV file, you can use pandas to skip the header row and read the file from line 2. Here's how you can do it:

```python
import pandas as pd

data = pd.read_csv('data.csv', skiprows=1)
```

In this code snippet, the `read_csv()` function from pandas is used to read the CSV file. The `skiprows` parameter is set to 1 to skip the first row (the header row). The resulting `data` variable contains the data from the CSV file starting from the second row.

Using pandas to read a file from line 2 has the advantage of being more versatile than the previous methods. You can easily read CSV files with any number of rows and that have header rows at any position in the file. However, it requires pandas to be installed and you need to be familiar with using pandas.
