---
title: Compare two dataframes and display side-by-side the variances between them
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: The easiest way to output the differences between two DataFrames in Python is by using pandas` `merge()` function with the `indicator=True` parameter, which will add a column to the resulting DataFrame indicating the source of each row.
---

**Contents**

[TOC]

## Importing Required Libraries and DataFrames:

Firstly, we need to import the required libraries to work with the DataFrames. We will be using pandas library to read and compare the DataFrames. Also, we will create two sample DataFrames to showcase how to compare them.

``` python
# Importing Required Libraries
import pandas as pd

# Creating First Sample DataFrame
df1 = pd.DataFrame({'A': [1, 2, 3, 4],
                   'B': [5, 6, 7, 8],
                   'C': [9, 10, 11, 12]})

# Creating Second Sample DataFrame
df2 = pd.DataFrame({'A': [1, 2, 3, 5],
                   'B': [5, 6, 7, 8],
                   'C': [9, 10, 13, 12]})
```

Here, we have created two sample DataFrames df1 and df2.


## Using Pandas 'compare' Function:

We can use the pandas library's 'compare' function to compare the two DataFrames. This function takes two DataFrames as input and returns the differences between them as output. We need to pass the two DataFrames and provide the join type to compare them.

``` python
# Comparing DataFrames using 'compare' Function
df3 = df1.compare(df2, keep_shape=True)

# Printing the Output
print(df3)
```

Here, we have compared the DataFrames df1 and df2 using the 'compare' function. We have also set the 'keep_shape' parameter to True, which keeps the shape of the output DataFrame the same as the input DataFrames. Finally, we have printed the output to display the differences between the DataFrames.


## Output:

We can see the output contains the following columns:
    
* 'A_left': This column shows the values in column 'A' from the left DataFrame (df1)
* 'A_right': This column shows the values in column 'A' from the right DataFrame (df2)
* 'B': This column shows the values in column 'B' from both the DataFrames
* 'C_left': This column shows the values in column 'C' from the left DataFrame (df1)
* 'C_right': This column shows the values in column 'C' from the right DataFrame (df2)

We can see that there is a difference in values in column 'A' and 'C' between the two DataFrames. This output can help us identify the differences between two DataFrames and can be used to perform further operations like merging, filtering, etc.
