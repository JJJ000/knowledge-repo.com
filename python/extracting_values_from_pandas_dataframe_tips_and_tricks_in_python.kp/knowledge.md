---
title: What is the way to extract a value from a pandas dataframe that is not the index or object type?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the `.iloc` or `.at` method to access a specific row and column of the DataFrame, and then use the `.values` attribute to return the value as a numpy array or Python scalar, respectively.
---

**Contents**

[TOC]

Section 1: Introduction

Pandas is a popular library in Python used to manipulate and analyze data. One of its core data structures is the DataFrame, which is a two-dimensional labeled array that can hold data of different types. In some cases, you may need to extract a value from a specific cell in the DataFrame. However, when you try to do this using the conventional indexing method, you may get an object type instead of the value you were expecting. In this tutorial, we will explore different methods to extract the value from a Pandas DataFrame.

Section 2: Accessing a single value with the .at attribute

The .at attribute is a fast and efficient way to extract a single value from a DataFrame. It takes two parameters: the row label and the column label. Here is an example of how to use it:

```
import pandas as pd

# creating a sample DataFrame
data = {
    'Name': ['John', 'Jane', 'Peter', 'Mary'],
    'Age': [30, 25, 40, 35],
    'Gender': ['M', 'F', 'M', 'F']
}

df = pd.DataFrame(data)

# accessing a single value with the .at attribute
age = df.at[1, 'Age']

print(age)   # Output: 25
```

In this example, we created a sample DataFrame and used the .at attribute to extract the value in the second row and the 'Age' column.

Section 3: Accessing a single value with the .iloc attribute

The .iloc attribute is another way to extract a single value from a DataFrame. It takes two parameters: the row index and the column index. Here is an example of how to use it:

```
import pandas as pd

# creating a sample DataFrame
data = {
    'Name': ['John', 'Jane', 'Peter', 'Mary'],
    'Age': [30, 25, 40, 35],
    'Gender': ['M', 'F', 'M', 'F']
}

df = pd.DataFrame(data)

# accessing a single value with the .iloc attribute
age = df.iloc[1, 1]

print(age)   # Output: 25
```

In this example, we used the .iloc attribute to extract the value in the second row and the second column.

Section 4: Conclusion

In conclusion, there are several ways to extract a value from a Pandas DataFrame. The .at attribute is a fast and efficient way to extract a single value based on the row and column labels, while the .iloc attribute can be used to extract a single value based on the row and column indexes. By using these methods, you can extract the value you need from the DataFrame without getting an object type.
