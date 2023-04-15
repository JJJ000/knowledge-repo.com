---
title: Converting empty cells (containing white spaces) into nan using pandas
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Use the replace method with the parameter ```` for the blank value and replace it with `np.NaN`. 

Example `df.replace(``, np.NaN)` where `df` is your pandas dataframe and `np` is the numpy library which includes the NaN value.
---

**Contents**

[TOC]

Section 1: Importing pandas
To begin replacing blank values with NaN in pandas, we need to import the pandas module. We can do this using the import statement in Python.

```python
import pandas as pd
```

Section 2: Reading in data
Once we have imported pandas, we need to read in the data that we want to process. We can do this using the read_csv() function in pandas, which reads in data from a CSV file and stores it in a pandas DataFrame.

```python
df = pd.read_csv('data.csv')
```

In this example, we are reading in data from a file called 'data.csv' and storing it in a DataFrame called df.

Section 3: Replacing blank values with NaN
Now that we have our data stored in a pandas DataFrame, we can replace any blank values with NaN using the replace() function in pandas. We can specify the blank value using a regular expression (regex).

```python
df.replace(r'^\s*$', np.nan, regex=True, inplace=True)
```

In this example, we are using a regular expression that matches any white space (^\s*$) and replacing it with NaN. The regex=True parameter tells pandas to interpret the search string as a regular expression, and the inplace=True parameter tells pandas to modify the DataFrame in place rather than creating a new DataFrame.

Section 4: Writing out data
Once we have replaced the blank values with NaN in our DataFrame, we can write out the data to a new CSV file using the to_csv() function.

```python
df.to_csv('clean_data.csv', index=False)
```

In this example, we are writing out the cleaned data to a file called 'clean_data.csv', with the index=False parameter telling pandas not to write out the row index as a column in the CSV file.
