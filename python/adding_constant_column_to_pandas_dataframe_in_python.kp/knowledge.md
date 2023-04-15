---
title: Include a column with a consistent value into a pandas dataframe
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the following code to add a new column `new\_col` with a constant value of 100 to a pandas dataframe df df[`new\_col`] = 100.
---

**Contents**

[TOC]

Section 1: Creating a sample dataframe
To demonstrate how to add a column with a constant value to a pandas dataframe, we first need to create a sample dataframe. We can do this by importing pandas and creating a dictionary with some sample data:

```python
import pandas as pd

data = {'name': ['John', 'Jane', 'Sam', 'Adam'],
        'age': [30, 25, 32, 45],
        'city': ['New York', 'Los Angeles', 'Chicago', 'Houston']}
df = pd.DataFrame(data)
print(df)
```

This will give us the following dataframe:

|   | name | age | city        |
|---|------|-----|-------------|
| 0 | John | 30  | New York    |
| 1 | Jane | 25  | Los Angeles |
| 2 | Sam  | 32  | Chicago     |
| 3 | Adam | 45  | Houston     |

Section 2: Adding a column with a constant value
To add a column with a constant value to our dataframe, we can simply use the assignment operator to create a new column and assign it a constant value. For example, let's add a new column called 'gender' with a constant value of 'M':

```python
df['gender'] = 'M'
print(df)
```

This will add a new column to our dataframe with the constant value 'M':

|   | name | age | city        | gender |
|---|------|-----|-------------|--------|
| 0 | John | 30  | New York    | M      |
| 1 | Jane | 25  | Los Angeles | M      |
| 2 | Sam  | 32  | Chicago     | M      |
| 3 | Adam | 45  | Houston     | M      |

Section 3: Adding a column with a constant value using 'insert'
Another way of adding a column with a constant value is to use the 'insert' method. This method allows us to specify the position of the new column in the dataframe. For example, let's add a new column called 'status' with a constant value of 'Single' at position 2:

```python
df.insert(2, 'status', 'Single')
print(df)
```

This will add a new column to our dataframe called 'status' with the constant value 'Single':

|   | name | age | status | city        | gender |
|---|------|-----|--------|-------------|--------|
| 0 | John | 30  | Single | New York    | M      |
| 1 | Jane | 25  | Single | Los Angeles | M      |
| 2 | Sam  | 32  | Single | Chicago     | M      |
| 3 | Adam | 45  | Single | Houston     | M      |

Section 4: Adding a column with a constant value using 'assign'
Finally, we can also use the 'assign' method to add a column with a constant value. This method allows us to chain multiple methods together and create a new dataframe with the added column. For example, let's add a new column called 'salary' with a constant value of 5000:

```python
df = df.assign(salary=5000)
print(df)
```

This will create a new dataframe with the added column 'salary' and the constant value of 5000:

|   | name | age | status | city        | gender | salary |
|---|------|-----|--------|-------------|--------|--------|
| 0 | John | 30  | Single | New York    | M      | 5000   |
| 1 | Jane | 25  | Single | Los Angeles | M      | 5000   |
| 2 | Sam  | 32  | Single | Chicago     | M      | 5000   |
| 3 | Adam | 45  | Single | Houston     | M      | 5000   |

Conclusion:
Adding a column with a constant value to a pandas dataframe is a simple task that can be done in multiple ways. We can use the assignment operator, insert method or assign method to add a column with a constant value. Depending on the scenario, one method may be more suitable than another.
