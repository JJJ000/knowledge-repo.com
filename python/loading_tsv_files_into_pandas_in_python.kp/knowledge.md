---
title: What is the process for loading a tsv file into a pandas dataframe?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: To load a tsv file into a Pandas DataFrame in Python, use the `read\_csv()` method and specify the `delimiter=`\t`` argument.
---

**Contents**

[TOC]

## 1. Importing Libraries

The first step in loading a TSV file into a Pandas DataFrame is to import the necessary libraries. In this case, we will be importing Pandas - a popular library used for data manipulation and analysis in Python.

```python
import pandas as pd
```

## 2. Loading the TSV file

Once the Pandas library has been imported, the next step is to load the TSV file into a Pandas DataFrame. We can use the `read_csv()` function in Pandas to load TSV files. The `read_csv()` function takes a few parameters to customize the loading process such as:

- `filepath`: the path or URL to the TSV file
- `delimiter`: the delimiter used in the file (in this case, it is a tab)
- `header`: whether the file has a header row, and if so, which row to use as column headers
- `index_col`: which column to use as the index (if any)


```python
df = pd.read_csv('file.tsv', delimiter='\t', header=0, index_col=None)
```

## 3. Exploring the Data

Once the TSV file has been loaded into a Pandas DataFrame, we can start exploring and analyzing the data. We can use several built-in functions in Pandas to get a better understanding of the data. Some of the most commonly used functions are:

- `df.head()`: Returns the first n rows of the DataFrame (default is 5)
- `df.tail()`: Returns the last n rows of the DataFrame (default is 5)
- `df.info()`: Provides a summary of the DataFrame, including the number of rows and columns, data types, and memory usage
- `df.describe()`: Provides summary statistics for the numerical columns in the DataFrame, such as mean, standard deviation, and quartiles.

```python
# To view the first 5 rows of the DataFrame
df.head()

# To view the last 5 rows of the DataFrame
df.tail()

# To get a summary of the DataFrame
df.info()

# To view summary statistics for numerical columns
df.describe()
```

## 4. Exporting the Data

Once we have analyzed and processed the data, we may want to export it to a new file. We can use the `to_csv()` function in Pandas to export the DataFrame to a CSV file. We can customize the exporting process using parameters such as:

- `filepath`: the name and path of the CSV file to be created
- `sep`: the column delimiter to use (in this case, ",", which is the default delimiter for a CSV file)
- `index`: whether to include the index (row labels) in the exported file or not
- `header`: whether to include the header row in the exported file or not


```python
df.to_csv('new_file.csv', sep=',', index=False, header=True)
```

This will create a new CSV file called "new_file.csv" in the current working directory.
