---
title: Replace the values in a column of pandas dataframe, depending on a particular condition
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: You can use the `.loc` method and a conditional statement to replace all values in a specific column of a pandas DataFrame based on a condition, like this 

```
df.loc[df[`column\_name`] == condition, `column\_name`] = new\_value
```
---

**Contents**

[TOC]

Section 1: Introduction
In Python, the Pandas library is widely used for handling and processing data. A pandas DataFrame is a two-dimensional, size-mutable, tabular, and a series-like data structure that is commonly used for data manipulation, analysis, and visualization. Updating or replacing values in a pandas DataFrame column based on a certain condition is a common requirement while working with data. In this guide, we shall discuss how to replace all values in a pandas DataFrame column based on a certain condition in Python.

Section 2: Replace values in a column based on condition
To replace values in a pandas DataFrame column based on a certain condition, we can use the loc() function of the DataFrame along with the boolean indexing. Here’s how we can do it.

* Firstly, we create our pandas DataFrame as follows:

```python
import pandas as pd

data = {'Name': ['John', 'Mick', 'Alice', 'Bob'],
        'Age': [28, 22, 25, 24],
        'Salary': [5000, 4500, 3000, 3500]}

df = pd.DataFrame(data)
```

* Now, let’s suppose we want to replace all values in the Salary column greater than 4000 with a value of 4000. Here’s how we can do it:

```python
df.loc[df['Salary'] > 4000, 'Salary'] = 4000
```
In this code, we are using boolean indexing to create a boolean mask that selects all the rows where the Salary value is greater than 4000. The boolean mask is passed as the row selector while accessing the column Salary using the loc() function of the DataFrame. 

Section 3: Verify the replacement
To confirm that the replacement was carried out successfully, we can use the print() function to print the updated pandas DataFrame:

```python
print(df)
```
Output:

|    | Name   |   Age |   Salary |
|---:|:-------|------:|---------:|
|  0 | John   |    28 |     4000 |
|  1 | Mick   |    22 |     4000 |
|  2 | Alice  |    25 |     3000 |
|  3 | Bob    |    24 |     3500 |

Here, we can see that the Salary values in rows 0 and 1 were updated to 4000, as they were greater than 4000.

Section 4: Conclusion
In this guide, we discussed how to replace all values in a pandas DataFrame column based on a certain condition in Python. We used the boolean indexing and loc() function to create a boolean mask that selects the rows based on the condition and updates the desired column. The same approach can be used for different data types and conditions.
