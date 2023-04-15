---
title: What is the method to eliminate the spaces between subplots in matplotlib?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Use the `plt.subplots\_adjust()` function and adjust the `hspace` and `wspace` parameters to reduce the gaps between subplots in Matplotlib.
---

**Contents**

[TOC]

## Section 1: Understanding subplot spacing in matplotlib

In matplotlib, when you create a figure with multiple subplots (using `plt.subplots()` or `fig.add_subplot()`), there is a default spacing between the subplots. This spacing is controlled by the `subplot_adjust()` function, which is called automatically when you create subplots. By default, the spacing is set to:

`plt.subplots_adjust(wspace=0.4, hspace=0.4)`

Here, `wspace` and `hspace` are the horizontal and vertical spacing between subplots, respectively. 

## Section 2: Removing gaps between subplots

If you want to remove the gaps between subplots, you can simply set the `wspace` and `hspace` arguments to 0 when creating the subplots:

```python
fig, axes = plt.subplots(nrows=2, ncols=2, figsize=(8, 6), gridspec_kw={'wspace':0, 'hspace':0})
```

Here, we've set the `wspace` and `hspace` arguments to 0 using the `gridspec_kw` parameter.

## Section 3: Adjusting subplot spacing

If you want to adjust the spacing between subplots to a custom value, you can use the `subplot_adjust()` function. 

```python
fig, axes = plt.subplots(nrows=2, ncols=2, figsize=(8, 6))

plt.subplots_adjust(wspace=0.2, hspace=0.2)
```

Here, we've set the `wspace` and `hspace` arguments to 0.2. This will create a small gap between subplots.

## Section 4: Adjusting subplot spacing for specific subplots

You can also adjust the spacing between specific subplots by targeting them individually using their index:

```python
fig, axes = plt.subplots(nrows=2, ncols=2, figsize=(8, 6))

plt.subplots_adjust(wspace=0.2, hspace=0.2)

# Adjust spacing between subplots 1 and 2
plt.subplots_adjust(hspace=0.3, wspace=0.3, bottom=0.1, top=0.9, left=0.1, right=0.9)

# Adjust spacing between subplots 2 and 3
plt.subplots_adjust(hspace=0.1, wspace=0.1, bottom=0.1, top=0.9, left=0.1, right=0.9)
```

Here, we've adjusted the spacing between subplots 1 and 2 using `hspace` and `wspace`, and the spacing between subplots 2 and 3 using `hspace` and `wspace`. We've also used the `bottom`, `top`, `left`, and `right` arguments to adjust the positioning and size of the subplots within the figure.
