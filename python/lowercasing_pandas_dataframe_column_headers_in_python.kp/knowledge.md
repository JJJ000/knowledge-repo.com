---
title: What is the method to convert all the column headers in a pandas dataframe to lowercase?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can make pandas dataframe column headers all lowercase by using the `.lower()` method on the column names `df.columns = df.columns.str.lower()`.
---

**Contents**

[TOC]

## Introduction

In data analysis, it is common to have data with headers that are in uppercase letters, lowercase letters, or a mix of both. It is usually a good practice to have uniformity in the header names, either in uppercase or lowercase. In this tutorial, we will see different ways of making pandas dataframe column headers all lowercase in Python.

## Prerequisites

Before we proceed, make sure to have pandas installed in your Python environment. You can install pandas using the command: 

```python
!pip install pandas
```

After installing pandas, let's import it.

```python
import pandas as pd
```

## Sample Data

To demonstrate how to make pandas dataframe column headers all lowercase, we will use a sample dataset. Let's create a pandas dataframe with one column in uppercase and another column in lowercase:

```python
data = {'Name': ['Alice', 'Bob', 'Charlie'], 'age': [25, 30, 35]}
df = pd.DataFrame(data)
```

The dataframe `df` looks like this:

```
       Name  age
0     Alice   25
1       Bob   30
2  Charlie   35
```

## Using the `str.lower()` method

The simplest way to make pandas dataframe column headers all lowercase is by using the `str.lower()` method. This method is available on columns of the dataframe as well as the dataframe itself.

To apply the `str.lower()` method to the dataframe columns, we can use the `columns` attribute of the dataframe and set it to the lowercase value of the existing column names:

```python
df.columns = df.columns.str.lower()
```

After executing this line of code, the column headers of the dataframe `df` will be all lowercase. The resulting dataframe looks like this:

```
       name  age
0     Alice   25
1       Bob   30
2  Charlie   35
```

## Using the `rename()` method

Another way to make pandas dataframe column headers all lowercase is by using the `rename()` method. The `rename()` method can be used to rename one or more columns of a dataframe. Here's how we can use it to make all column headers lowercase:

```python
df = df.rename(columns=str.lower)
```

This line of code renames all the columns of the dataframe `df` to lowercase using the `str.lower` method. This method returns a lowercase version of the string passed to it, and it is applied to each column name in the dataframe. The resulting dataframe looks like this:

```
       name  age
0     Alice   25
1       Bob   30
2  Charlie   35
```

## Conclusion

In this tutorial, we saw different ways to make pandas dataframe column headers all lowercase in Python. We used the `str.lower()` method to directly convert column headers to lowercase, and the `rename()` method to rename columns to lowercase. Either one can be used, depending on what works for you. Using lowercase column headers makes our data easy to work with and avoids errors that might arise due to mixed cases.
