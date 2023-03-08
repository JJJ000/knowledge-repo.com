---
title: Pick out rows from pandas based on the index specified in a list
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: To select Pandas rows based on list index in Python, you can use the .iloc method with the index values in a list.
---

**Contents**

[TOC]

# Section 1: Creating sample data

In this section, we will create a sample Pandas DataFrame that we will use to demonstrate how to select rows based on list index in Python.

```python
import pandas as pd

# Creating a sample DataFrame
data = {
    'Name': ['John', 'Alice', 'Bob', 'Mary', 'Peter'],
    'Age': [25, 30, 35, 40, 45],
    'Country': ['USA', 'Canada', 'Australia', 'UK', 'France']
}
df = pd.DataFrame(data)

# Printing the DataFrame
print(df)
```

Output:
```
    Name  Age    Country
0   John   25        USA
1  Alice   30     Canada
2    Bob   35  Australia
3   Mary   40         UK
4  Peter   45     France
```

# Section 2: Selecting rows based on list index

In this section, we will select rows from the sample DataFrame based on a list of index values.

```python
# Selecting rows based on a list of index values
index_list = [0, 2, 4]
selected_rows = df.iloc[index_list]

# Printing the selected rows
print(selected_rows)
```

Output:
```
    Name  Age    Country
0   John   25        USA
2    Bob   35  Australia
4  Peter   45     France
```

# Section 3: Converting index selection to list

In this section, we will convert the selected rows to a list.

```python
# Converting the selected rows to a list
selected_rows_list = selected_rows.values.tolist()

# Printing the selected rows list
print(selected_rows_list)
```

Output:
```
[['John', 25, 'USA'], ['Bob', 35, 'Australia'], ['Peter', 45, 'France']]
```

# Section 4: Using list comprehension

In this section, we will use list comprehension to select rows from the DataFrame based on a list of index values.

```python
# Selecting rows based on a list of index values using list comprehension
index_list = [0, 2, 4]
selected_rows = [df.iloc[i].tolist() for i in index_list]

# Printing the selected rows
print(selected_rows)
```

Output:
```
[['John', 25, 'USA'], ['Bob', 35, 'Australia'], ['Peter', 45, 'France']]
```
