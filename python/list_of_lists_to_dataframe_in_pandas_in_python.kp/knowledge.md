---
title: Converting a list of lists into a pandas dataframe
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Use the pandas DataFrame constructor and pass the list of lists as the data parameter.
---

**Contents**

[TOC]

## Section 1: Understanding the problem statement

To convert a list of lists into a pandas DataFrame in Python, we need to define the following:

- What is a list of lists?
- What is a pandas DataFrame?
- How can we get a list of lists into a pandas DataFrame?

## Section 2: List of Lists

A list of lists is a container that holds multiple lists inside it. Each inner list can contain any number of elements, and the list of lists can hold any number of inner lists.

Example of a list of lists:
```python
list_of_lists = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
```

## Section 3: Pandas DataFrame

A pandas DataFrame is a two-dimensional size-mutable, tabular data structure. It allows us to handle and manipulate data in a structured way. It has rows and columns, and each column can have a different data type. It is the most commonly used data structure in pandas.

Example of a pandas DataFrame:
```python
import pandas as pd

data = {'Name': ['John', 'Sam', 'Ann'],
        'Age': [23, 36, 29],
        'Salary': [55000, 72000, 62000]}

df = pd.DataFrame(data)
```

## Section 4: Converting List of Lists to Pandas DataFrame

To convert a list of lists to a pandas DataFrame, we need to follow these steps:

1. Import the pandas library:
```python
import pandas as pd
```

2. Create the list of lists:
```python
list_of_lists = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
```

3. Convert the list of lists to a pandas DataFrame using the pd.DataFrame() method:
```python
df = pd.DataFrame(list_of_lists)
```

The resulting DataFrame will have the same number of rows and columns as the list of lists.
