---
title: Determine how often a particular value appears in a dataframe column
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: You can use the value\_counts() method to count the frequency of values in a dataframe column in Python.
---

**Contents**

[TOC]

## Solution
### Section 1: Setting Up
The first step is to create a dataframe and assign it to a variable.

```python
import pandas as pd

# create a dataframe
df = pd.DataFrame({'A': [1, 2, 3, 1, 2, 3, 1, 2, 3], 
                   'B': [4, 5, 6, 4, 5, 6, 4, 5, 6],
                   'C': [7, 8, 9, 7, 8, 9, 7, 8, 9]})
```

### Section 2: Counting Frequency
The second step is to use the `value_counts()` function to count the frequency of each value in the column.

```python
# count the frequency of values in column A
frequency_counts = df['A'].value_counts()

# print the results
print(frequency_counts)
```

The output of the above code is:

```
1    3
2    3
3    3
Name: A, dtype: int64
```

### Section 3: Sorting Results
The third step is to sort the results in descending order.

```python
# sort the results in descending order
frequency_counts = df['A'].value_counts(ascending=False)

# print the results
print(frequency_counts)
```

The output of the above code is:

```
3    3
2    3
1    3
Name: A, dtype: int64
```

### Section 4: Converting Results to Dictionary
The fourth step is to convert the results to a dictionary.

```python
# convert the results to a dictionary
frequency_dict = frequency_counts.to_dict()

# print the results
print(frequency_dict)
```

The output of the above code is:

```
{3: 3, 2: 3, 1: 3}
```
