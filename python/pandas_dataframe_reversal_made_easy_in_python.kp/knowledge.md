---
title: What is the correct method for reversing a pandas dataframe?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: The right way to reverse a pandas DataFrame in Python is to use the .iloc[-1] indexer.
---

**Contents**

[TOC]

1. Introduction

Reversing a pandas DataFrame means reversing the order of its rows or columns. Sometimes we may need to reverse a DataFrame to display the data in descending order or to perform some analysis on the reversed data. There are several ways to reverse a pandas DataFrame in Python. In this guide, we will discuss some of the commonly used methods.

2. Reversing Rows

To reverse the rows of a pandas DataFrame, we can use the `iloc` accessor with a negative index. Consider the following example:

```python
import pandas as pd

# create a sample DataFrame
data = {'name': ['John', 'Alice', 'Bob', 'Mary'],
        'age': [25, 18, 40, 32],
        'city': ['New York', 'London', 'Paris', 'Tokyo']}
df = pd.DataFrame(data)

# reverse the rows
df_rev = df.iloc[::-1]
print(df_rev)
```

This will produce the following output:

```
    name  age      city
3   Mary   32     Tokyo
2    Bob   40     Paris
1  Alice   18    London
0   John   25  New York
```

As we can see, the `iloc[::-1]` syntax reverses the order of rows in the DataFrame.

3. Reversing Columns

To reverse the columns of a pandas DataFrame, we can use the `iloc` accessor again, but this time we need to specify `[:, ::-1]`. Here's an example:

```python
import pandas as pd

# create a sample DataFrame
data = {'name': ['John', 'Alice', 'Bob', 'Mary'],
        'age': [25, 18, 40, 32],
        'city': ['New York', 'London', 'Paris', 'Tokyo']}
df = pd.DataFrame(data)

# reverse the columns
df_rev = df.iloc[:, ::-1]
print(df_rev)
```

This will produce the following output:

```
       city  age   name
0  New York   25   John
1    London   18  Alice
2     Paris   40    Bob
3     Tokyo   32   Mary
```

As we can see, the `iloc[:, ::-1]` syntax reverses the order of columns in the DataFrame.

4. Reversing both Rows and Columns

If we want to reverse both the rows and columns of a pandas DataFrame, we can combine the two `iloc` accessors. Here's an example:

```python
import pandas as pd

# create a sample DataFrame
data = {'name': ['John', 'Alice', 'Bob', 'Mary'],
        'age': [25, 18, 40, 32],
        'city': ['New York', 'London', 'Paris', 'Tokyo']}
df = pd.DataFrame(data)

# reverse both rows and columns
df_rev = df.iloc[::-1, ::-1]
print(df_rev)
```

This will produce the following output:

```
       city  age   name
3     Tokyo   32   Mary
2     Paris   40    Bob
1    London   18  Alice
0  New York   25   John
```

As we can see, the `iloc[::-1, ::-1]` syntax reverses both the rows and columns of the DataFrame.

5. Conclusion

In this guide, we have discussed some of the commonly used methods to reverse a pandas DataFrame in Python. Depending on our requirements, we can choose any of these methods to reverse the rows, columns, or both in a DataFrame. By reversing the order of the data, we can gain new insights into the data and perform data analysis tasks more effectively.
