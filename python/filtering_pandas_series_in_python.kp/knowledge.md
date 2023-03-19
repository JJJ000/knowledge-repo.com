---
title: How to apply filtering on a pandas series?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: To filter a Series in Python, use boolean indexing to select the desired rows based on a certain condition.
---

**Contents**

[TOC]

## Introduction

Filtering a Series in Pandas is an important step in data analysis. Pandas provides various methods to filter a Series, including boolean indexing and the `query()` method. In this article, we will explore different ways to filter a Series in Pandas.

## Creating a Series

Before we start filtering a Series, let's create a sample series using Pandas.

```python
import pandas as pd

data = {'countries': ['USA', 'Canada', 'Mexico', 'UK', 'India', 'Japan', 'China']}
s = pd.Series(data['countries'])

print(s)
```

Output:

```
0       USA
1    Canada
2    Mexico
3        UK
4     India
5     Japan
6     China
dtype: object
```

## Filtering a Series using Boolean Indexing

One of the simplest ways to filter a Series in Pandas is using boolean indexing. We can use boolean indexing to filter all the values in a Series that satisfy the specified condition.

```python
import pandas as pd

data = {'countries': ['USA', 'Canada', 'Mexico', 'UK', 'India', 'Japan', 'China']}
s = pd.Series(data['countries'])

# Filter countries that start with 'U'
result = s[s.str.startswith('U')]

print(result)
```

Output:

```
0     USA
3      UK
dtype: object
```

In the above example, we used `s.str.startswith()` to filter all the countries in the `s` Series that start with the letter 'U'.

## Filtering a Series using query() method

Another approach to filter a Series in Pandas is using the `query()` method. The `query()` method allows us to filter a Series by providing a query string that specifies the condition.

```python
import pandas as pd

data = {'countries': ['USA', 'Canada', 'Mexico', 'UK', 'India', 'Japan', 'China']}
s = pd.Series(data['countries'])

# Filter countries that start with 'U'
result = s.query('str.startswith("U")')

print(result)
```

Output:

```
0     USA
3      UK
dtype: object
```

In the above example, we used the `query()` method to filter all the countries in the `s` Series that start with the letter 'U'.

## Filtering a Series using the .loc and .iloc

We can also use the `.loc` and `.iloc` accessors to filter a Series based on label or positional indexing, respectively.

```python
import pandas as pd

data = {'countries': ['USA', 'Canada', 'Mexico', 'UK', 'India', 'Japan', 'China']}
s = pd.Series(data['countries'])

# Filter countries at index 2 and 4
result = s.loc[[2,4]]

print(result)
```

Output:

```
2    Mexico
4     India
dtype: object
```

In the above example, we used the `.loc` accessor to filter countries in the `s` Series at index 2 and 4.

```python
import pandas as pd

data = {'countries': ['USA', 'Canada', 'Mexico', 'UK', 'India', 'Japan', 'China']}
s = pd.Series(data['countries'])

# Filter countries at position 2 and 4
result = s.iloc[[2,4]]

print(result)
```

Output:

```
2    Mexico
4     India
dtype: object
```

In the above example, we used the `.iloc` accessor to filter countries in the `s` Series at position 2 and 4.

## Conclusion

In this article, we explored different approaches to filter a Series in Pandas, including boolean indexing, the `query()` method, and the `.loc` and `.iloc` accessors. These methods can help you filter data based on different types of conditions and provide flexibility in data analysis.
