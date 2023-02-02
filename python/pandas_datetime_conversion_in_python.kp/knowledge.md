---
title: Change pandas column to datetime format
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Use the pd.to\_datetime() method to convert a Pandas column to DateTime.
---

**Contents**

[TOC]

## Section 1: Importing Necessary Packages

In order to convert a Pandas column to DateTime, we will need to import the `pandas` and `datetime` packages. 

```python
import pandas as pd
import datetime as dt
```

## Section 2: Creating a Pandas DataFrame

We can create a Pandas DataFrame with a column of dates in string format.

```python
# Create a dictionary of dates
dates = {'date': ['2020-01-01', '2020-02-01', '2020-03-01']}

# Create a DataFrame
df = pd.DataFrame(dates)

# Print the DataFrame
print(df)
```

Output:

|    | date       |
|---:|:-----------|
|  0 | 2020-01-01 |
|  1 | 2020-02-01 |
|  2 | 2020-03-01 |

## Section 3: Converting the DataFrame to DateTime

We can use the `pd.to_datetime()` function to convert the `date` column to DateTime.

```python
# Convert the date column to DateTime
df['date'] = pd.to_datetime(df['date'])

# Print the DataFrame
print(df)
```

Output:

|    | date       |
|---:|:-----------|
|  0 | 2020-01-01 |
|  1 | 2020-02-01 |
|  2 | 2020-03-01 |

## Section 4: Verifying the Conversion

We can use the `dtype` attribute to verify that the `date` column has been converted to DateTime.

```python
# Check the data type of the date column
print(df['date'].dtype)
```

Output: `datetime64[ns]`
