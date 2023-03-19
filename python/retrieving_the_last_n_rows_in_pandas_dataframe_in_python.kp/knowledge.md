---
title: What is the method to retrieve the last n rows of a pandas dataframe?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the `.tail(n)` method on the DataFrame, where n is the number of rows to retrieve.
---

**Contents**

[TOC]

Section 1: Introduction
-----------------------

Pandas is an open-source data analysis library for Python. It is widely used by data scientists and analysts because of its flexibility, power, and ease of use. In this tutorial, we will learn how to get the last N rows of a pandas DataFrame in Python.

Section 2: Method 1 - tail()
-----------------------------

Pandas provides a simple method called `tail()` that returns the last N rows of a DataFrame. The `tail()` method takes an optional parameter `n` that specifies the number of rows to return. By default, `n` is set to 5. Here's an example:

```
import pandas as pd 

# create a DataFrame
data = {'Name': ['John', 'Alex', 'Maria', 'Joseph', 'Anna'], 
        'Age': [25, 19, 23, 31, 27], 
        'Country': ['USA', 'Canada', 'Spain', 'France', 'Italy']} 

df = pd.DataFrame(data) 

# get the last 3 rows 
last_rows = df.tail(3) 

print(last_rows)
```

Output:

```
    Name  Age Country
2  Maria   23   Spain
3  Joseph   31  France
4   Anna   27   Italy
```

Section 3: Method 2 - iloc()
-----------------------------

Another way to get the last N rows of a DataFrame is to use the `iloc()` method. The `iloc()` method is used to select data based on its position. Here's an example:

```
import pandas as pd 

# create a DataFrame
data = {'Name': ['John', 'Alex', 'Maria', 'Joseph', 'Anna'], 
        'Age': [25, 19, 23, 31, 27], 
        'Country': ['USA', 'Canada', 'Spain', 'France', 'Italy']} 

df = pd.DataFrame(data) 

# get the number of rows in the DataFrame 
n = len(df) 

# get the last 3 rows 
last_rows = df.iloc[n-3:n] 

print(last_rows)
```

Output:

```
    Name  Age Country
2  Maria   23   Spain
3  Joseph   31  France
4   Anna   27   Italy
```

Section 4: Conclusion
----------------------

In this tutorial, we learned two ways to get the last N rows of a pandas DataFrame in Python. The `tail()` method is the simplest way to achieve this, while the `iloc()` method provides more flexibility and control over the selection process. Depending on the use case, either of these methods can be used to get the desired result.
