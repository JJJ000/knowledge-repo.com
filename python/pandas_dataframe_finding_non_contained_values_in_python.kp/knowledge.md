---
title: Look for 'not containing' values in a pandas dataframe
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: The `does-not-contain` functionality can be achieved by using the `~` (tilde) operator in combination with the `str.contains()` method when searching for values within a Pandas DataFrame in Python.
---

**Contents**

[TOC]

## Introduction
In this tutorial, we will learn how to search for "does-not-contain" on a DataFrame in pandas in Python. 

## Example Dataset
To illustrate the concept of "does-not-contain" on a DataFrame, we will create a sample dataset containing information about six cities and their corresponding countries as shown below.


``` python
import pandas as pd

data = {'City': ['Lagos', 'Paris', 'Rio de Janeiro', 'Melbourne', 'Kuala Lumpur', 'New York'], 
        'Country': ['Nigeria', 'France', 'Brazil', 'Australia', 'Malaysia', 'United States']}

df = pd.DataFrame(data)

print(df)
```

```
            City        Country
0          Lagos        Nigeria
1          Paris         France
2  Rio de Janeiro         Brazil
3       Melbourne      Australia
4    Kuala Lumpur       Malaysia
5       New York  United States
```
## Using the "~" symbol to indicate "does-not-contain"
To search for values that do not contain a specific string pattern in a DataFrame column, we can use the "~" symbol in combination with the str.contains() method. 

``` python 
# search for all rows that do not contain the word "ari" in the 'City' column

result = df[~df['City'].str.contains('ari')]
print(result)
```

output:

```
         City        Country
0       Lagos        Nigeria
3    Melbourne      Australia
4  Kuala Lumpur       Malaysia
5     New York  United States
```

From the output, we can see that the query returned all rows that do not contain the string 'ari' in the 'City' column.

## Using the notna() method to search for rows with non-null values
The notna() method can be used to search for all rows with non-null values in a DataFrame column. We can then negate the query using the "~" symbol to find rows with null values.

``` python
import numpy as np 

# add a null value to the 'Country' column
df.loc[6] = ['Beijing', np.nan]

# search for all rows with non-null values in the 'Country' column
result = df[df['Country'].notna()]

# search for all rows with null values in the 'Country' column
null_result = df[~df['Country'].notna()]

print(result)
print(null_result)
```

output:

```
            City        Country
0          Lagos        Nigeria
1          Paris         France
2  Rio de Janeiro         Brazil
3       Melbourne      Australia
4    Kuala Lumpur       Malaysia
5       New York  United States
            City Country
6        Beijing     NaN
```

From the output, we can see that the query returned all rows with non-null values in the 'Country' column. The second query returned only the row with a null value in the 'Country' column. 


## Conclusion 
In this tutorial, we have learned how to search for "does-not-contain" on a DataFrame in pandas in Python. We used the "~" symbol in combination with the str.contains() and notna() methods to find all rows that do not contain a specific string pattern and all rows with null values in a DataFrame column respectively.
