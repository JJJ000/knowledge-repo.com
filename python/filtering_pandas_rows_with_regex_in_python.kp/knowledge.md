---
title: What is the method to apply regex to filter rows in pandas?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the `str.contains()` method in pandas with a regular expression pattern to filter rows based on text matches.
---

**Contents**

[TOC]

## Section 1: Importing Necessary Libraries

Pandas library needs to be imported along with any other required libraries. 

```python
import pandas as pd
```


## Section 2: Creating Sample DataFrame
 
We'll create a sample dataframe to demonstrate the filtering process. 

```python
data = {'Name': ['John', 'Mike', 'Sarah', 'Charlie'],
        'Age': [25, 35, 28, 19],
        'Salary': [50000, 70000, 65000, 45000],
        'Address': ['23 Hardwick Road', '17 Elmwood Drive', '19 Westwood Lane', '11 Albert Street']
       }

df = pd.DataFrame(data)
```

## Section 3: Using Regex to Filter Rows

In pandas, `.str.contains()` function can be used to filter rows based on a regex pattern. We can use this function on a dataframe column to filter rows that match or do not match a particular pattern. 

```python
#keep rows where Name column starts with 'S'
new_df = df[df['Name'].str.contains('^S')]
print(new_df)
```

This would print the following output:

```
    Name  Age  Salary          Address
2  Sarah   28   65000  19 Westwood Lane
```

Here `^S` means that the Name column should start with 'S'. We could also use `[^S]` to exclude rows with 'S' in the Name column.

## Section 4: Combining Multiple Patterns

We can also combine multiple patterns using the '|' operator. The '|' operator here allows filtering based on multiple regex patterns.

```python
#keep rows where Name column starts with 'S' or has 'e' in it
new_df = df[df['Name'].str.contains('^S|e')]
print(new_df)
```

This would print the following output:

```
    Name  Age  Salary            Address
1   Mike   35   70000  17 Elmwood Drive
2  Sarah   28   65000    19 Westwood Lane
```

Here `^S|e` means that the Name column should either start with 'S' or have 'e' in it.
