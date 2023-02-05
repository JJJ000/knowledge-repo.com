---
title: How can I create a single colorbar for multiple subplots?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the same colorbar instance for each subplot by calling pyplot.colorbar() with the same mappable object for each subplot.
---

**Contents**

[TOC]

1.  Setup the Figure and Axes

Before creating the subplots, you need to set up the figure and axes. This can be done using the `plt.subplots()` function. This function takes in the number of rows and columns of the desired subplots and returns the figure and axes objects. 

2. Create the Subplots

Next, you need to create the subplots. This can be done using the `ax.imshow()` function for each axes object. This function takes in the data to be plotted, and any other desired parameters, such as the colormap.

3. Create the Colorbar

Once the subplots have been created, you can create the colorbar. This can be done using the `plt.colorbar()` function. This function takes in the axes object, and any other desired parameters, such as the colormap.

4. Adjust the Colorbar

Finally, you can adjust the colorbar by setting the `ax.cax.colorbar()` property. This property takes in the desired parameters, such as the colorbar label, orientation, and size.
