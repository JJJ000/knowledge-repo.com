---
title: What is the procedure for altering the dimensions of a seaborn axes or figure level plot?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: You can use the `figsize` argument of the seaborn plotting function to change the figure size of a seaborn plot.
---

**Contents**

[TOC]

#### Section 1: Adjust Figure Size at Axes Level

To adjust the figure size of a seaborn axes level plot in Python, use the `figsize` argument when calling the `sns.set()` function. For example:

```python
sns.set(figsize=(10,8))
```

This will set the figure size to 10 inches by 8 inches.

#### Section 2: Adjust Figure Size at Figure Level

To adjust the figure size of a seaborn figure level plot in Python, use the `figsize` argument when calling the `plt.figure()` function. For example:

```python
fig = plt.figure(figsize=(10,8))
```

This will set the figure size to 10 inches by 8 inches.

#### Section 3: Adjust Figure Size at Subplot Level

To adjust the figure size of a seaborn subplot level plot in Python, use the `figsize` argument when calling the `plt.subplots()` function. For example:

```python
fig, ax = plt.subplots(figsize=(10,8))
```

This will set the figure size to 10 inches by 8 inches.

#### Section 4: Adjust Figure Size at Facet Level

To adjust the figure size of a seaborn facet level plot in Python, use the `figsize` argument when calling the `sns.FacetGrid()` function. For example:

```python
g = sns.FacetGrid(data, figsize=(10, 8))
```

This will set the figure size to 10 inches by 8 inches.
