---
title: Reworded 'identify the distinct groupings of data in specific columns within a pandas dataframe and calculate their frequencies.'
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To get the unique combinations of values in selected columns in a Pandas data frame and count them in Python, use the following syntax df.groupby([`col1`, `col2`]).size().reset\_index(name=`count`).
---

**Contents**

[TOC]

# Section 1: Setting up the Data Frame

To demonstrate how to find unique combinations of values and count them in pandas data frame, we first need to set up a sample data frame. We can create a sample data frame with the Pandas library.

```python
import pandas as pd

data = {'Name': ['John', 'Jane', 'Bob', 'Sarah', 'Mike', 'Matt'],
        'City': ['New York', 'Paris', 'London', 'Sydney', 'New York', 'London'],
        'Gender': ['M', 'F', 'M', 'F', 'M', 'M'],
        'Age': [32, 25, 45, 29, 36, 27],
        'Product': ['A', 'C', 'B', 'A', 'B', 'C'],
        'Quantity': [2, 1, 3, 2, 4, 1]}

df = pd.DataFrame(data)
```

This will create a data frame with Name, City, Gender, Age, Product, and Quantity columns.

# Section 2: Finding Unique Combinations of Values

To find unique combinations of values in selected columns, we can use the `groupby` function in pandas. We first need to specify which columns we want to group by, and then we can use the `nunique` function to count the number of unique combinations.

```python
unique_combinations = df.groupby(['Gender', 'Product']).nunique()

print(unique_combinations)
```

This will group the data frame by Gender and Product columns and count the number of unique combinations for each group. 

# Section 3: Filtering the Results

We can filter the results to only show the counts for unique combinations that occur more than once. We can use the `filter` function to apply a condition to the data frame.

```python
unique_combinations = unique_combinations.filter(lambda x: x['Name'] > 1)

print(unique_combinations)
```

This will filter the data frame to only show the counts for unique combinations that occur more than once in the Name column.

# Section 4: Resetting the Index

To reset the index of the data frame, we can use the `reset_index` function.

```python
unique_combinations = unique_combinations.reset_index()

print(unique_combinations)
```

This will reset the index of the data frame to a numerical index. The data frame will have three columns: Gender, Product, and Name. The Name column will show the counts for each unique combination that occurs more than once.
