---
title: What is the process for iterating through columns in a pandas dataframe in order to perform regression analysis?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use a for loop to iterate over the columns and run regression on each column.
---

**Contents**

[TOC]

### Getting started with pandas
First, we need to import the pandas library and read in our data as a dataframe. We can use the `read_csv()` function to read in a CSV file as a dataframe.

```python
import pandas as pd

# Read in data as dataframe
df = pd.read_csv('data.csv')
```

### Iterating over columns
To iterate over the columns in our dataframe, we can use a `for` loop to loop through the column names. We can retrieve the names of the columns using the `.columns` attribute of the dataframe.

```python
# Iterate over columns in dataframe
for col in df.columns:
    print(col)
```

### Running regression on each column
To run a regression on each column, we can use the `statsmodels` library. We can create a function that takes in a column name, fits a linear regression model, and returns the results.

```python
import statsmodels.api as sm

# Define function to run regression on column
def run_regression(column_name):
    X = df[column_name]
    y = df['target_variable']
    X = sm.add_constant(X)
    model = sm.OLS(y, X).fit()
    return model.summary()
```

### Running regression on all columns
Now that we have a function to run a regression on a single column, we can iterate over all of the columns in our dataframe and run the regression on each.

```python
# Loop through columns and run regression on each
for col in df.columns:
    if col != 'target_variable':  # Skip target variable
        print('\n' + col.upper())
        print(run_regression(col))
```

This will print out a summary of the regression results for each column in our dataframe, skipping the target variable.
