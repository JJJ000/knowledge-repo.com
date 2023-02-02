---
title: Creating a legend for pyplot in matplotlib in the easiest way
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Add a call to plt.legend() after plotting the data.
---

**Contents**

[TOC]

**1. Create the Legend**

To create a legend in Matplotlib, we need to use the `plt.legend()` function. This function takes a list of labels as an argument, and it will create a legend with each label corresponding to a different color or marker.

**2. Add Labels to Plot**

Before creating the legend, we need to add labels to our plot. This can be done using the `plt.xlabel()` and `plt.ylabel()` functions. We can also add a title to the plot using the `plt.title()` function.

**3. Create the Legend**

Now that we have added labels to our plot, we can create the legend. We can do this by passing a list of labels to the `plt.legend()` function. The labels should correspond to the colors or markers used in the plot.

**4. Adjust the Legend**

Finally, we can adjust the legend by specifying a location, font size, and other properties. The `plt.legend()` function has several optional arguments that can be used to customize the legend.
