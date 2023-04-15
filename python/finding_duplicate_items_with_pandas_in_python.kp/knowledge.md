---
title: What is the method to obtain a list of all the replicated elements using pandas in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: df[df.duplicated()]
---

**Contents**

[TOC]

Section 1: Importing the necessary libraries

We need to import the pandas library to work with dataframes.

```python
import pandas as pd
```

Section 2: Loading the dataset

We need to load the dataset into a pandas dataframe. We can do this using the `read_csv` function of pandas.

```python
data = pd.read_csv('path/to/dataset.csv')
```

Section 3: Identifying duplicate items

We can use the `duplicated` function of pandas to identify duplicate items. This function returns a boolean series indicating for each row whether it's a duplicate or not. We can then use this boolean series to filter the dataframe to get all the duplicate items.

```python
duplicate_series = data.duplicated()
duplicate_data = data[duplicate_series]
```

Section 4: Getting the list of all duplicate items

Finally, we can use the `values` attribute of the duplicate data dataframe to get all the duplicate items as a numpy array.

```python
duplicates = duplicate_data.values
``` 

The variable `duplicates` will now contain a numpy array of all the duplicate items.
