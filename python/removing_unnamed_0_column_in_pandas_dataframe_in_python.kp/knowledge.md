---
title: What is the method to remove the "unnamed 0" column from a pandas dataframe that has been read from a csv file?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: To get rid of the `Unnamed 0` column in a pandas DataFrame, use the parameter `index\_col` while reading the CSV file setting it to 0, and then reassign the modified dataframe to the original variable.
---

**Contents**

[TOC]

## Section 1: Reading in the CSV file

To start with, we need to read in the CSV file using `pandas.read_csv()`. This will create a DataFrame containing all of the data in the CSV file.

``` python
import pandas as pd

data = pd.read_csv('filename.csv')
```

## Section 2: Removing the Unnamed: 0 column

If the CSV file includes an index column, it will be read in as an additional column named `Unnamed: 0`. This column can be removed using the `drop()` method of the DataFrame.

``` python
data = data.drop('Unnamed: 0', axis=1)
```

In the above code, `axis=1` specifies that we want to drop a column rather than a row. The modified DataFrame is then stored back in the `data` variable.

## Section 3: Writing the modified DataFrame to a new CSV file

You may want to write the modified DataFrame to a new CSV file. This can be done using the `to_csv()` method of the DataFrame.

``` python
data.to_csv('new_filename.csv', index=False)
```

In the above code, `index=False` specifies that we do not want to write out the index column. 

## Section 4: Combining the above steps

The above steps can be combined into a single code block as shown below:

``` python
import pandas as pd

# Read in the CSV file
data = pd.read_csv('filename.csv')

# Remove the Unnamed: 0 column
data = data.drop('Unnamed: 0', axis=1)

# Write the modified DataFrame to a new CSV file
data.to_csv('new_filename.csv', index=False)
```

The output will be a new CSV file (named `new_filename.csv`) that is identical to the input file, except that the `Unnamed: 0` column has been removed.
