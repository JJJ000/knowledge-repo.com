---
title: Get the value of a column by using another column as a reference in pandas
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Use boolean indexing to filter rows based on a condition in one column and then select the values in another column using the .loc accessor.
---

**Contents**

[TOC]

There are multiple ways to extract column values based on another column in Pandas. Some of them are:

1. Using Boolean Indexing
---
In this method, we create a Boolean condition based on the values of a column and use it to filter out the required values from another column. Here's how it works in code:

```python
import pandas as pd

# create a sample dataframe
df = pd.DataFrame({
   'name': ['Alice', 'Bob', 'Charlie', 'Dave', 'Ellen'],
   'age': [25, 34, 19, 42, 28],
   'gender': ['F', 'M', 'M', 'M', 'F']
})

# filter out ages of males
male_ages = df.loc[df['gender']=='M', 'age']
print(male_ages)
```

Output:
```
1    34
2    19
3    42
Name: age, dtype: int64
```

Here, we used the Boolean condition `df['gender']=='M'` to filter out only the rows where the value in the 'gender' column is 'M'. Then, we used the `.loc[]` function to extract only the values in the 'age' column for these rows.


2. Using .loc() function for updating values based on another column.
---
We can also use the `.loc[]` function to update the values of a column based on the values of another column. Here's how:

```python
import pandas as pd

# create a sample dataframe
df = pd.DataFrame({
   'name': ['Alice', 'Bob', 'Charlie', 'Dave', 'Ellen'],
   'age': [25, 34, 19, 42, 28],
   'gender': ['F', 'M', 'M', 'M', 'F']
})

# update ages of males to be 30
df.loc[df['gender']=='M', 'age'] = 30
print(df)
```

Output:
```
      name  age gender
0    Alice   25      F
1      Bob   30      M
2  Charlie   30      M
3     Dave   30      M
4    Ellen   28      F
```

Here, we used the Boolean condition `df['gender']=='M'` to filter out only the rows where the value in the 'gender' column is 'M'. Then, we used the `.loc[]` function to update the values in the 'age' column for these rows to be 30.


3. Using the .apply() function with a lambda function
---
We can also use the `.apply()` function with a lambda function to extract column values based on another column. Here's how:

```python
import pandas as pd

# create a sample dataframe
df = pd.DataFrame({
   'name': ['Alice', 'Bob', 'Charlie', 'Dave', 'Ellen'],
   'age': [25, 34, 19, 42, 28],
   'gender': ['F', 'M', 'M', 'M', 'F']
})

# extract names of males
male_names = df[df['gender']=='M'].apply(lambda x: x['name'], axis=1)
print(male_names)
```

Output:
```
1        Bob
2    Charlie
3       Dave
dtype: object
```

Here, we used the Boolean condition `df['gender']=='M'` to filter out only the rows where the value in the 'gender' column is 'M'. Then, we used the `.apply()` function with a lambda function to extract only the values in the 'name' column for these rows. The `axis=1` parameter tells Pandas to apply the lambda function across rows instead of columns.
