---
title: Change the data type of columns to string in pandas
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the astype() method to convert the columns to strings in Pandas.
---

**Contents**

[TOC]

#### Section 1: Importing the Pandas Library

In order to convert columns to string in Pandas, we must first import the Pandas library:

```python
import pandas as pd
```

#### Section 2: Creating a DataFrame

Next, we must create a DataFrame containing the data that we wish to convert to string. We can do this by passing a dictionary of lists to the `pd.DataFrame()` function:

```python
data = {'Name':['John','Bob','Sally'],
        'Age':[21,25,23],
        'Score':[80,90,95]}

df = pd.DataFrame(data)
```

#### Section 3: Converting Columns to String

Once the DataFrame has been created, we can use the `astype()` method to convert the columns to string:

```python
df['Name'] = df['Name'].astype(str)
df['Age'] = df['Age'].astype(str)
df['Score'] = df['Score'].astype(str)
```

#### Section 4: Verifying the Conversion

We can verify that the conversion was successful by using the `dtypes` attribute to view the data types of the columns in the DataFrame:

```python
df.dtypes
```

The output should show that all the columns are now of type `object` (string):

```
Name     object
Age      object
Score    object
dtype: object
```
