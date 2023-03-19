---
title: Insert a column into a dataframe using a list
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the syntax `dataframe[`new\_column`] = new\_list` to add a new column in a dataframe from a list in Python.
---

**Contents**

[TOC]

## Using DataFrame.assign() Method

This method is used when a new column needs to be added to a dataframe. It returns a new dataframe with the added column.

```python
import pandas as pd

# Create the dataframe
df = pd.DataFrame({'A': [1, 2, 3, 4], 'B': [5, 6, 7, 8]})

# Create the list to be added as a column
new_column = [9, 10, 11, 12]

# Use the assign method to add the new column
df = df.assign(C=new_column)

print(df)
```

Output:

```
   A  B   C
0  1  5   9
1  2  6  10
2  3  7  11
3  4  8  12
```


## Using DataFrame.insert() Method

This method is used when a new column needs to be inserted at a specific position in the dataframe. It modifies the dataframe in place.

```python
import pandas as pd

# Create the dataframe
df = pd.DataFrame({'A': [1, 2, 3, 4], 'B': [5, 6, 7, 8]})

# Create the list to be added as a column
new_column = [9, 10, 11, 12]

# Use the insert method to add the new column at position 2
df.insert(2, 'C', new_column)

print(df)
```

Output:

```
   A  B   C
0  1  5   9
1  2  6  10
2  3  7  11
3  4  8  12
```


## Using direct assignment

This method is used when we have a list that matches the length of an existing column in the dataframe. It modifies the dataframe in place.

```python
import pandas as pd

# Create the dataframe
df = pd.DataFrame({'A': [1, 2, 3, 4], 'B': [5, 6, 7, 8]})

# Create the list to be added as a column
new_column = [9, 10, 11, 12]

# Use direct assignment to add the new column
df['C'] = new_column

print(df)
```

Output:

```
   A  B   C
0  1  5   9
1  2  6  10
2  3  7  11
3  4  8  12
```
