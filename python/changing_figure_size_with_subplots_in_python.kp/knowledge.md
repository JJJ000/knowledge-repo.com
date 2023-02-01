---
title: What is the best way to adjust the size of my subplots?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: You can change the figure size of subplots in Python by using the figsize argument in the plt.subplots() function.
---

**Contents**

[TOC]

1. **Using `plt.subplots()`**

The `plt.subplots()` function can be used to create a figure and axes objects in one step. This function takes two arguments: the number of rows and columns of subplots. The `figsize` argument allows you to specify the size of the figure.

For example, to create a figure with two subplots with a width of 10 inches and a height of 8 inches, use the following code: 

```
fig, ax = plt.subplots(2, 1, figsize=(10, 8))
```

2. **Using `plt.figure()`**

The `plt.figure()` function can be used to create a figure object. This function takes the `figsize` argument, which allows you to specify the size of the figure.

For example, to create a figure with a width of 10 inches and a height of 8 inches, use the following code: 

```
fig = plt.figure(figsize=(10, 8))
```

3. **Using `ax.set_figsize()`**

The `ax.set_figsize()` method can be used to set the size of an axes object. This method takes two arguments: the width and height of the figure.

For example, to set the size of an axes object to 10 inches by 8 inches, use the following code: 

```
ax.set_figsize(10, 8)
```

4. **Using `fig.set_size_inches()`**

The `fig.set_size_inches()` method can be used to set the size of a figure object. This method takes two arguments: the width and height of the figure.

For example, to set the size of a figure object to 10 inches by 8 inches, use the following code: 

```
fig.set_size_inches(10, 8)
```
