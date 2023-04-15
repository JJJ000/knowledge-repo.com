---
title: What is the way to determine the dimensions or structure of a dataframe in pyspark?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The size or shape of a DataFrame in PySpark can be found using the `count` and `columns` methods respectively.
---

**Contents**

[TOC]

# Checking the shape of a DataFrame in PySpark

To get the shape of a DataFrame (number of rows and columns), there are two methods available in PySpark - `count()` and `describe()`. 

## Using `count()`:

The `count()` method returns the number of rows in a DataFrame. To get the number of columns, we can use the `len()` function on the DataFrame's `columns` property. 

```python
# Create a sample DataFrame
df = spark.createDataFrame([(1, "John", "Doe"), 
                            (2, "Jane", "Doe"), 
                            (3, "Bob", "Smith")], 
                           ["id", "firstname", "lastname"])

# Get the shape of the DataFrame using count()
rows = df.count()
cols = len(df.columns)

print(f"Number of rows: {rows}")
print(f"Number of columns: {cols}")

# Output:
# Number of rows: 3
# Number of columns: 3
```

## Using `describe()`:

The `describe()` method returns statistical information about the DataFrame. One of the outputs is the number of rows (count) and the number of columns. We can filter out the count and select the relevant information. 

```python
# Create a sample DataFrame
df = spark.createDataFrame([(1, "John", "Doe"), 
                            (2, "Jane", "Doe"), 
                            (3, "Bob", "Smith")], 
                           ["id", "firstname", "lastname"])

# Get the shape of the DataFrame using describe()
shape = df.describe().filter("summary = 'count'").select(*df.columns).collect()[0]

print(f"Number of rows: {shape[0]}")
print(f"Number of columns: {len(shape)}")

# Output:
# Number of rows: 3
# Number of columns: 3
```

Note that the `describe()` method returns a DataFrame, so we need to filter and select the information we need. The `collect()` method returns a list of Row objects, so we need to access the relevant information by index.
