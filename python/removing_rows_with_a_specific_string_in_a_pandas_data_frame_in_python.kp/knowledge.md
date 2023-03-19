---
title: What is the procedure to eliminate rows from a pandas data frame that have a particular string in a specific column?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: To drop rows from a Pandas dataframe that contain a particular string in a particular column, use df = df[~df[`column\_name`].str.contains(`string\_to\_drop`)].
---

**Contents**

[TOC]

## Section 1: Introduction
In this tutorial, we will learn how to drop rows from a Pandas data frame that contains a particular string in a particular column in Python. Deleting or removing rows is a common data cleaning task that is necessary when dealing with large datasets that have missing or irrelevant data.

## Section 2: Reading the Data Frame
First, we need to read the data frame using the `pandas.read_csv()` function. In this tutorial, we will use the Titanic data set from Kaggle. We will read the data into a Pandas data frame using the following code:

```python
import pandas as pd

# Read the data frame from the CSV file
df = pd.read_csv('titanic.csv')
```

## Section 3: Dropping Rows that Contain a Particular String
Next, we will use the `pandas.DataFrame.drop()` function to drop rows that contain a particular string in a particular column. In this tutorial, we will drop all rows that contain the string 'female' in the 'sex' column. Here is the code:

```python
# Drop rows that contain 'female' in the 'sex' column
df = df.drop(df[df['sex'] == 'female'].index)
```

The `df[df['sex'] == 'female']` command selects all the rows where the 'sex' column contains the string 'female', and the `.index` attribute returns the index of those rows. Finally, the `df.drop()` function removes the selected rows from the data frame.

## Section 4: Writing the Data Frame
Finally, we can write the updated data frame to a CSV file using the `pandas.DataFrame.to_csv()` function. Here is the final code:

```python
# Write the updated data frame to a CSV file
df.to_csv('titanic_updated.csv', index=False)
```

The `index=False` argument ensures that the row index is not written to the CSV file.
