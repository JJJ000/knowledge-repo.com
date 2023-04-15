---
title: Eliminating replicate items from a series of lists
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Create a set of tuples and convert it back to a list of lists.
---

**Contents**

[TOC]

## Method 1: Using sets and list comprehension

One of the simplest ways to remove duplicates from a list of lists is by using sets and list comprehension. This approach involves flattening the list of lists into a single list of elements, converting it into a set to remove duplicates, and then converting it back into a list.

Here's an example code snippet that demonstrates this approach:

```python
lst = [[1, 2], [2, 3], [3, 4], [4, 5], [1, 2], [3, 4]]
new_lst = list(set([tuple(elem) for elem in lst]))
```

In this example, we first create a list of lists `lst` containing some duplicate elements. We then use list comprehension to flatten the list into a list of tuples using `tuple(elem) for elem in lst`. We then create a set from this list of tuples using `set(...)`, which automatically removes duplicates. Finally, we convert the set back into a list of lists using `list(...)`, giving us the desired output in `new_lst`.


## Method 2: Using for loops and a temporary list

Another approach to removing duplicates from a list of lists is to use for loops and a temporary list to keep track of seen elements. This approach involves iterating over each element in the list of lists, checking if it has been seen before, and appending it to the output list if it hasn't.

Here's an example code snippet that demonstrates this approach:

```python
lst = [[1, 2], [2, 3], [3, 4], [4, 5], [1, 2], [3, 4]]
new_lst = []
seen = []

for elem in lst:
    if elem not in seen:
        new_lst.append(elem)
        seen.append(elem)
```

In this example, we first create a list of lists `lst` containing some duplicate elements. We then create an empty list `new_lst` to store the unique elements and another empty list `seen` to keep track of the elements we've already seen. We then iterate over each element in `lst`, checking if it has been seen before using `if elem not in seen`. If it hasn't been seen, we append it to `new_lst` and add it to `seen`. Finally, we return `new_lst`, which contains only the unique elements.


## Method 3: Using the pandas library

Another option to remove duplicates from a list of lists is using the pandas library. This library provides a powerful and efficient set of data structures and tools for data manipulation and analysis. The `pandas.DataFrame` class has a `drop_duplicates()` method that can be used to remove duplicate rows from a dataframe, including a list of lists.

Here's an example code snippet that demonstrates this approach:

```python
import pandas as pd

lst = [[1, 2], [2, 3], [3, 4], [4, 5], [1, 2], [3, 4]]
df = pd.DataFrame(lst)
new_df = df.drop_duplicates()

new_lst = new_df.values.tolist()
```

In this example, we first create a list of lists `lst` containing some duplicate elements. We then convert this list into a pandas DataFrame using `pd.DataFrame(lst)`. We then use the `drop_duplicates()` method to remove any duplicate rows from the dataframe. Finally, we convert the dataframe back into a list of lists using `new_df.values.tolist()`, giving us the desired output in `new_lst`. Note that using the pandas library may be overkill for small lists, but it can be extremely efficient for large datasets.
