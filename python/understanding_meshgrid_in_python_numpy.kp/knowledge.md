---
title: What does meshgrid do in Python / numpy?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Meshgrid is used to create a rectangular grid out of an array of x and y coordinates.
---

**Contents**

[TOC]

### Overview
Meshgrid is a NumPy function that is used to create a rectangular grid out of an array of x values and an array of y values. It is used to evaluate functions on a grid and to generate 2-D arrays which can be used as input to other functions.

### Functionality
Meshgrid takes two 1-D arrays and produces two 2-D arrays which represent all pairs of (x, y) in the two arrays. The resulting 2-D arrays can be used as input to functions which expect 2-D arrays as input. For example, the NumPy function ‘pcolormesh’ takes 2-D arrays as input and produces a pseudocolor plot.

### Applications
Meshgrid is used to create contour plots, surface plots and other visualizations which require evaluating functions on a grid. It is also used in machine learning algorithms such as support vector machines and k-nearest neighbors which require a grid of input points to evaluate the function.
