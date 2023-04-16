---
title: Creating different sized subplots with matplotlib
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Matplotlib can create different size subplots by using the plt.subplots() function and passing in the desired number of rows and columns.
---

**Contents**

[TOC]

**Section 1: Creating Subplots**

Matplotlib provides the `plt.subplots()` function to create subplots of different sizes. This function takes in the number of rows and columns of subplots as well as the size of each subplot as arguments. For example, to create a 2x2 grid of subplots with each subplot being 8 inches by 8 inches, the following code can be used:

```
fig, ax = plt.subplots(2, 2, figsize=(8, 8))
```

**Section 2: Adjusting Subplot Size**

The size of each subplot can be adjusted by passing in a tuple of (width, height) for each subplot as an argument to `plt.subplots()`. For example, to create a 2x2 grid of subplots with the top left subplot being 8 inches by 8 inches, the top right subplot being 4 inches by 8 inches, the bottom left subplot being 8 inches by 4 inches, and the bottom right subplot being 4 inches by 4 inches, the following code can be used:

```
fig, ax = plt.subplots(2, 2, figsize=((8, 8), (4, 8), (8, 4), (4, 4)))
```

**Section 3: Adjusting Individual Subplot Size**

If the size of each subplot needs to be adjusted individually, the `fig.set_size_inches()` function can be used. This function takes in a tuple of (width, height) as an argument and sets the size of the entire figure. To adjust the size of a single subplot, the `ax.set_size_inches()` function can be used. This function takes in a tuple of (width, height) and sets the size of the subplot. For example, to set the size of the top left subplot to 8 inches by 8 inches, the following code can be used:

```
ax[0, 0].set_size_inches((8, 8))
```

**Section 4: Saving Subplots**

The `plt.savefig()` function can be used to save the figure and its subplots. This function takes in the file name as an argument and saves the figure as an image file. For example, to save the figure as a PNG file, the following code can be used:

```
plt.savefig('figure.png')
```
