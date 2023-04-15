---
title: What is the process for determining the frequency of an item in a list?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the count() method to count the occurrences of a list item in Python.
---

**Contents**

[TOC]

# Using a For Loop

1. Create a list of items that you want to count the occurrences of.

```python
items = [1, 2, 3, 4, 1, 4, 5, 2, 4, 5]
```

2. Create an empty dictionary to store the count of each item.

```python
counts = {}
```

3. Iterate through the list of items and increment the count of each item in the dictionary.

```python
for item in items:
    if item in counts:
        counts[item] += 1
    else:
        counts[item] = 1
```

4. Print the counts of each item.

```python
for item in counts:
    print(f"{item}: {counts[item]}")
```

# Using Counter

1. Create a list of items that you want to count the occurrences of.

```python
items = [1, 2, 3, 4, 1, 4, 5, 2, 4, 5]
```

2. Import the Counter class from the collections module.

```python
from collections import Counter
```

3. Create a Counter object and pass the list of items to it.

```python
counts = Counter(items)
```

4. Print the counts of each item.

```python
for item in counts:
    print(f"{item}: {counts[item]}")
```
