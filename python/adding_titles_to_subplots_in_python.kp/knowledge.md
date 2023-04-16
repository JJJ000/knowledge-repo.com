---
title: What is the process for adding a title to each subplot?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the plt.title() function to add a title to each subplot.
---

**Contents**

[TOC]

### Section 1: Set Up Subplots

First, you need to set up the subplots. This is done using the `plt.subplots()` function. This function takes in the number of rows and columns of the subplots, and returns a Figure and an array of Axes objects.

```
fig, axes = plt.subplots(nrows, ncols)
```

### Section 2: Set Up Titles

Once the subplots are created, you can set up titles for each subplot. This can be done by accessing each Axes object from the array and setting the `title` attribute. 

```
for ax in axes.flatten():
    ax.set_title("Title for Subplot")
```

### Section 3: Customize Titles

You can also customize the titles for each subplot. This can be done by passing in a dictionary of keyword arguments to the `title` attribute. 

```
title_kwargs = {
    'fontsize': 16, 
    'fontweight': 'bold', 
    'color': 'red'
}

for ax in axes.flatten():
    ax.set_title("Title for Subplot", **title_kwargs)
```

### Section 4: Show Plots

Finally, you can show the plots using the `plt.show()` function. 

```
plt.show()
```
