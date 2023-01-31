---
title: What are the statistical calculations (e.g. count, mean, etc) for each group using pandas groupby?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Pandas GroupBy can be used to calculate various statistics such as count, mean, sum, min, max, etc. for each group.
---

**Contents**

[TOC]

**Section 1: Count**

The GroupBy.count() method can be used to count the number of observations in each group.

```python
df.groupby('group_column').count()
```

**Section 2: Mean**

The GroupBy.mean() method can be used to calculate the mean of the values in each group.

```python
df.groupby('group_column').mean()
```

**Section 3: Median**

The GroupBy.median() method can be used to calculate the median of the values in each group.

```python
df.groupby('group_column').median()
```

**Section 4: Standard Deviation**

The GroupBy.std() method can be used to calculate the standard deviation of the values in each group.

```python
df.groupby('group_column').std()
```
