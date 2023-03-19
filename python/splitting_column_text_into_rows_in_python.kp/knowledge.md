---
title: What are the steps to divide the text within a column into several rows?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: You can split text in a column into multiple rows in Python by using the split() function and then converting the resulting list into a pandas dataframe.
---

**Contents**

[TOC]

## Introduction
In this tutorial, we will learn how to split a text column into multiple rows in Python. For instance, consider a dataset that has a column containing a list of professions for each person. We can split this column to create new rows for each profession, and each row would have the same information for each person, except for the profession field.

## Step 1: Importing necessary Libraries

First, we need to import the pandas library for data manipulation and read the CSV file using the read_csv() function. 

```python
import pandas as pd

df = pd.read_csv('filename.csv')
```

## Step 2: Splitting text into rows

Now we're ready to split the text in the column into multiple rows. We can use the string method split() to separate the text into a list of values, and then use the DataFrame function explode() to create a new row for each value.

```python
df['Profession'] = df['Profession'].str.split(',')
df = df.explode('Profession')
```

The first line separates the string in each row by the comma delimiter and creates a list of values. The second line explodes the list of values and creates a new row for each profession.

## Step 3: Renaming the Column

The "Profession" column would now have multiple professions separated by commas. We can rename this column to "Professions" since each row would now have a single profession.

```python
df = df.rename(columns={'Profession':'Professions'})
```

This renames the column from "Profession" to "Professions".

## Step 4: Writing the output

Once we've completed the above steps, we can write the output back to a CSV file using the to_csv() function.

```python
df.to_csv('output.csv', index=False)
```

This writes the output to a CSV file with the name "output.csv" and index is set to False so that Pandas does not include the index column in the output. We can now open this file in any text editor, or spreadsheet software.


## Conclusion

In this tutorial, we learned how to split text in a column into multiple rows using Python. We did this using the Pandas library's split() method and the explode() function. We then renamed the column and wrote the output to a CSV file using the to_csv() function. By following these steps, we can easily split text columns with comma-separated values into multiple rows.
