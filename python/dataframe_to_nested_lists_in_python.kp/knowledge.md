---
title: Convert a pandas dataframe into a nested list
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: We can convert a Pandas DataFrame to a list of lists using the values attribute of the DataFrame followed by tolist() method.
---

**Contents**

[TOC]

Section 1: Introduction
In data analysis, Pandas DataFrame is one of the most commonly used data structures. While working with Pandas, you may need to convert a DataFrame to a list of lists in Python for various purposes such as passing it to a machine learning algorithm or writing it to a CSV file. In this tutorial, we will explore different methods to convert a Pandas DataFrame to a list of lists in Python.

Section 2: Using the to_numpy() function
The to_numpy() function is one of the easiest ways to convert a Pandas DataFrame to a list of lists. This function converts the DataFrame into a NumPy array, which can be converted into a list of lists using the tolist() function. Here's an example:

```
import pandas as pd

# Creating a sample DataFrame
df = pd.DataFrame({'column1': [1, 2, 3], 'column2': [4, 5, 6], 'column3': [7, 8, 9]})

# Converting DataFrame to a list of lists
list_of_lists = df.to_numpy().tolist()

print(list_of_lists)
```

Output:

```
[[1, 4, 7], [2, 5, 8], [3, 6, 9]]
```

Section 3: Using the values attribute
In addition to the to_numpy() function, we can also use the values attribute to convert a Pandas DataFrame to a list of lists. The values attribute returns a NumPy array representing the DataFrame, which can be converted into a list of lists using the tolist() function. Here's an example:

```
import pandas as pd

# Creating a sample DataFrame
df = pd.DataFrame({'column1': [1, 2, 3], 'column2': [4, 5, 6], 'column3': [7, 8, 9]})

# Converting DataFrame to a list of lists
list_of_lists = df.values.tolist()

print(list_of_lists)
```

Output:

```
[[1, 4, 7], [2, 5, 8], [3, 6, 9]]
```

Section 4: Using a for loop
Finally, we can also use a for loop to convert a Pandas DataFrame to a list of lists. In this method, we iterate over the rows of the DataFrame and append each row to a list. Here's an example:

```
import pandas as pd

# Creating a sample DataFrame
df = pd.DataFrame({'column1': [1, 2, 3], 'column2': [4, 5, 6], 'column3': [7, 8, 9]})

# Converting DataFrame to a list of lists
list_of_lists = []

for index, row in df.iterrows():
    current_row = [row['column1'], row['column2'], row['column3']]
    list_of_lists.append(current_row)

print(list_of_lists)
```

Output:

```
[[1, 4, 7], [2, 5, 8], [3, 6, 9]]
```

Conclusion:
In this tutorial, we explored different methods to convert a Pandas DataFrame to a list of lists in Python. Depending on the situation, we can choose the appropriate method that best fits our needs.
