---
title: What is the procedure for adjusting the dimensions of figures generated with matplotlib?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can change the size of figures drawn with Matplotlib in Python by setting the figure size using the figsize parameter.
---

**Contents**

[TOC]

### Setting Figure Size

The size of the figure can be set using the `figsize` argument of the `plt.figure()` function. The `figsize` argument takes a tuple of two values. The first value is the width and the second value is the height of the figure. For example:

```python
plt.figure(figsize=(10,8))
```

This will create a figure with width 10 and height 8.

### Setting Axes Size

The size of the axes can be set using the `set_size_inches` method of the `Axes` object. This method takes a tuple of two values, similar to the `figsize` argument. For example:

```python
ax = plt.axes()
ax.set_size_inches(10,8)
```

This will set the size of the axes to 10 by 8.

### Setting Subplot Size

The size of a subplot can be set using the `set_figwidth` and `set_figheight` methods of the `SubplotBase` object. These methods take a single value, which is the width or height of the subplot. For example:

```python
ax = plt.subplot(1,2,1)
ax.set_figwidth(10)
ax.set_figheight(8)
```

This will set the size of the subplot to 10 by 8.

### Setting Aspect Ratio

The aspect ratio of the figure can be set using the `set_aspect` method of the `Axes` object. This method takes a single value, which is the aspect ratio of the figure. For example:

```python
ax = plt.axes()
ax.set_aspect(1.0)
```

This will set the aspect ratio of the figure to 1.0.
