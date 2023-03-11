---
title: Revise the values of a row in pandas when a specific condition is satisfied
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: Use the `loc` function to select the rows and columns, specify the condition to be met, and assign the new values to the selected rows and columns.
---

**Contents**

[TOC]

Section 1: Overview
To update row values where a certain condition is met in Pandas in Python, we need to identify the specific rows and columns that need to be modified and then assign new values to these positions. This can be done using various methods that provide the ability to filter rows based on certain conditions, such as boolean indexing or query functions.

Section 2: Boolean Indexing
Boolean indexing allows us to select rows based on a certain condition and then modify the values in those rows. For example, we can select all the rows where the values in one column are greater than a certain value, and then assign a new value to another column in those rows. Here is an example code snippet:

```
import pandas as pd

# create a sample dataframe
data = {'Name': ['David', 'John', 'Amy', 'Peter'],
        'Age': [25, 30, 20, 35],
        'Salary': [50000, 60000, 45000, 70000]}

df = pd.DataFrame(data)

# select rows where Salary is greater than 55000
condition = df['Salary'] > 55000
df.loc[condition, 'Salary'] = 65000

print(df)
```

Output:

```
    Name  Age  Salary
0  David   25   50000
1   John   30   65000
2    Amy   20   45000
3  Peter   35   70000
```

In this example, we have selected all the rows where the salary is greater than 55000 using boolean indexing and then assigned a new value of 65000 to those rows in the Salary column.

Section 3: Query Function
Another way to update row values where a certain condition is met is to use the query function. This function allows us to filter rows with conditions expressed as strings. The syntax is as follows:

```
df.loc[df.query('condition').index, 'column'] = new_value
```

Here is an example code snippet:

```
import pandas as pd

# create a sample dataframe
data = {'Name': ['David', 'John', 'Amy', 'Peter'],
        'Age': [25, 30, 20, 35],
        'Salary': [50000, 60000, 45000, 70000]}

df = pd.DataFrame(data)

# update Salary column where Age is greater than 25
df.loc[df.query('Age > 25').index, 'Salary'] = 65000

print(df)
```

Output:

```
    Name  Age  Salary
0  David   25   50000
1   John   30   65000
2    Amy   20   45000
3  Peter   35   65000
```

In this example, we have filtered rows where the Age column is greater than 25 using the query function and then assigned a new value of 65000 to those rows in the Salary column.

Section 4: Conclusion
Updating row values where a certain condition is met in Pandas in Python can be done using various methods, such as boolean indexing or query functions. These methods allow us to select specific rows and columns and assign new values to them based on conditions. By using these methods, we can easily update row values in our dataframes and perform various data manipulation tasks.
