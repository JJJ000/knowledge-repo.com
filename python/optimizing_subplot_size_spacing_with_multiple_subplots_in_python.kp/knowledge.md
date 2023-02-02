---
title: Increase the size and distance between multiple subplots
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Increase the figure size and adjust the subplot parameters such as hspace and wspace.
---

**Contents**

[TOC]

**Section 1: Adjusting Subplot Size**

The size of each individual subplot can be adjusted by setting the `figsize` parameter when creating the figure. For example, the following code will create a figure with four subplots of size 8x8 inches:

```python
fig, axes = plt.subplots(2, 2, figsize=(8, 8))
```

**Section 2: Adjusting Subplot Spacing**

The spacing between subplots can be adjusted by setting the `wspace` and `hspace` parameters when creating the figure. For example, the following code will create a figure with four subplots with a horizontal space of 0.2 and a vertical space of 0.4:

```python
fig, axes = plt.subplots(2, 2, wspace=0.2, hspace=0.4)
```

**Section 3: Adjusting Subplot Layout**

The layout of the subplots can be adjusted by setting the `subplot_kw` parameter when creating the figure. This parameter accepts a dictionary of keyword arguments that are passed to each subplot. For example, the following code will create a figure with four subplots with a left margin of 0.2 and a top margin of 0.4:

```python
fig, axes = plt.subplots(2, 2, subplot_kw={'left': 0.2, 'top': 0.4})
```

**Section 4: Adjusting Subplot Labels**

The labels of each subplot can be adjusted by setting the `label` parameter when creating the figure. For example, the following code will create a figure with four subplots with labels of 'A', 'B', 'C', and 'D':

```python
fig, axes = plt.subplots(2, 2, labels=['A', 'B', 'C', 'D'])
```
