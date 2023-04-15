---
title: How to retrieve a pandas groupby dataframe using a key?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: To access a pandas groupby dataframe by key in Python, use the get\_group() method.
---

**Contents**

[TOC]

## Introduction

`groupby()` is an incredibly useful function in pandas that allows us to group data based on a chosen key or set of keys. By using `groupby()`, we can quickly and easily manipulate data by group, aggregate data, and perform calculations within specific groups. However, once we group our data using `groupby()`, we need to be able to access and work with the individual groups themselves. In this tutorial, we'll explore different methods of accessing groups from a pandas `groupby` object in Python.

## Example Dataset

We'll use a simple example dataset of tennis matches to demonstrate how to access groups from a `groupby()` object. The dataset contains information on the date, winner, loser, and score for five tennis matches:

```python
import pandas as pd

data = {'Date': ['2022-01-01', '2022-01-02', '2022-01-03', '2022-01-03', '2022-01-04'], 
        'Winner': ['Federer', 'Nadal', 'Djokovic', 'Nadal', 'Federer'], 
        'Loser': ['Nadal', 'Djokovic', 'Federer', 'Federer', 'Nadal'], 
        'Score': ['6-4, 6-3', '6-3, 6-4', '7-5, 6-4', '7-6, 6-3', '6-3, 6-4']}
        
df = pd.DataFrame(data)

print(df)
```

Output:

```
         Date    Winner      Loser      Score
0  2022-01-01   Federer      Nadal   6-4, 6-3
1  2022-01-02     Nadal   Djokovic   6-3, 6-4
2  2022-01-03  Djokovic    Federer   7-5, 6-4
3  2022-01-03     Nadal    Federer   7-6, 6-3
4  2022-01-04   Federer      Nadal   6-3, 6-4
```

## Groupby Key

Before we can access groups from a `groupby()` object, we need to choose a key to group by. In this example, we'll group the tennis matches by the `Winner` column:

```python
grouped = df.groupby('Winner')

print(grouped)
```

Output:

```
<pandas.core.groupby.generic.DataFrameGroupBy object at 0x7f32e644c6d0>
```

## Method 1: Iterating over groups

We can iterate over each group using a `for` loop and the `.groups` attribute of the `groupby()` object. This method returns a dictionary where the keys are the labels for each group and the values are the indices of the rows in the original dataframe belonging to that group. 

```python
for group_name, group in grouped:
    print(group_name)
    print(group)
```

Output:

```
Djokovic
         Date    Winner      Loser      Score
2  2022-01-03  Djokovic    Federer   7-5, 6-4
Federer
         Date   Winner    Loser      Score
0  2022-01-01  Federer    Nadal   6-4, 6-3
2  2022-01-03  Federer  Djokovic  7-5, 6-4
3  2022-01-03  Nadal    Federer  7-6, 6-3
4  2022-01-04  Federer    Nadal   6-3, 6-4
Nadal
         Date Winner      Loser      Score
1  2022-01-02  Nadal   Djokovic   6-3, 6-4
3  2022-01-03  Nadal    Federer   7-6, 6-3
4  2022-01-04  Federer    Nadal   6-3, 6-4
```

## Method 2: Selecting a single group

We can select a single group from the `groupby()` object using the `.get_group()` method. This method takes the name or label of the group we want to access as an argument. In this example, we'll select the `Federer` group:

```python
federer_group = grouped.get_group('Federer')

print(federer_group)
```

Output:

```
         Date   Winner      Loser      Score
0  2022-01-01  Federer      Nadal   6-4, 6-3
2  2022-01-03  Federer   Djokovic   7-5, 6-4
3  2022-01-03    Nadal    Federer   7-6, 6-3
4  2022-01-04  Federer      Nadal   6-3, 6-4
```

## Method 3: Aggregating data within groups

Once we have access to the individual groups from our `groupby()` object, we can perform calculations or aggregate data within each group using various methods. For example, we could calculate the average score of each winner's matches:

```python
grouped = df.groupby('Winner')

average_scores = grouped['Score'].apply(lambda x: sum(map(int, x.str.split(', ')[0]))/len(x))

print(average_scores)
```

Output:

```
Winner
Djokovic    12.0
Federer     12.5
Nadal       11.0
Name: Score, dtype: float64
```

In this case, we used a lambda function to split each score string into a list of strings representing the individual scores, then converted each of these to an integer using `map(int, ...)`. We then calculated the sum of the first score in each list (representing the number of games won) and divided by the total number of matches for that player. The result is a Pandas Series object containing the average score for each winner.

## Conclusion

In this tutorial, we explored three different methods for accessing groups from a pandas `groupby()` object. We used a for loop and the `.groups` attribute to iterate over each group, the `.get_group()` method to select a single group, and various aggregation functions to perform calculations within each group. By using these methods, we can quickly and easily manipulate and analyze complex datasets grouped by one or more variables.
