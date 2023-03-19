---
title: Changing a portion of the rows in a pandas dataframe
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: To modify a subset of rows in a pandas dataframe in Python, use boolean indexing to filter the required rows and then modify the desired columns using the .loc accessor.
---

**Contents**

[TOC]

# Introduction
Pandas is a popular data manipulation library in Python. It provides data structures for efficiently storing and manipulating large datasets. One of the common tasks in data manipulation is modifying a subset of rows in a pandas dataframe. In this tutorial, we will discuss various ways to modify a subset of rows in a pandas dataframe.

# Section 1: Modifying rows based on condition
One common way to modify a subset of rows is to select the rows based on some condition and modify them.

```python
import pandas as pd

# Create a sample dataframe
df = pd.DataFrame({'name': ['Alice', 'Bob', 'Charlie', 'David'],
                   'score': [65, 78, 82, 91]})

# Modify the rows with score > 80
df.loc[df['score'] > 80, 'score'] = 100

print(df)
```

Output:
```
       name  score
0     Alice     65
1       Bob     78
2  Charlie    100
3     David    100
```

In the above example, we have modified the rows where the score is greater than 80 by setting it to 100.

# Section 2: Modifying rows by index
Another way to modify a subset of rows is to select the rows by their indices.

```python
import pandas as pd

# Create a sample dataframe
df = pd.DataFrame({'name': ['Alice', 'Bob', 'Charlie', 'David'],
                   'score': [65, 78, 82, 91]})

# Modify the rows with indices 1 and 2
df.loc[[1, 2], 'score'] = [80, 85]

print(df)
```

Output:
```
       name  score
0     Alice     65
1       Bob     80
2  Charlie     85
3     David     91
```

In the above example, we have modified the rows with indices 1 and 2 by setting their scores to 80 and 85 respectively.

# Section 3: Modifying rows using a function
We can also modify a subset of rows by applying a function to the rows.

```python
import pandas as pd

# Create a sample dataframe
df = pd.DataFrame({'name': ['Alice', 'Bob', 'Charlie', 'David'],
                   'score': [65, 78, 82, 91]})

# Modify the rows with score > 80 using a function
def add_bonus(score):
    return score + 10

df.loc[df['score'] > 80, 'score'] = df.loc[df['score'] > 80, 'score'].apply(add_bonus)

print(df)
```

Output:
```
       name  score
0     Alice     65
1       Bob     78
2  Charlie     92
3     David    101
```

In the above example, we have applied a function that adds 10 to the scores of the rows where the score is greater than 80.

# Conclusion
In this tutorial, we have discussed various ways to modify a subset of rows in a pandas dataframe. We have shown how to modify rows based on condition, by index, and using a function. Depending on the task at hand, one approach may be more suitable than the others.
