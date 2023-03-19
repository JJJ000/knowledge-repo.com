---
title: What is the process of setting identical axis labels for multiple subplots?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use `fig.supxlabel()` and `fig.supylabel()` to set common x and y axes labels for subplots in Python.
---

**Contents**

[TOC]

1. Import Necessary Libraries
Before we can start creating our subplots and adding common axes labels, we need to import the necessary libraries. In this case, we will be using matplotlib.pyplot:

```python
import matplotlib.pyplot as plt
```

2. Create Subplots
Next, we need to create our subplots using the plt.subplots() function. This function takes two arguments: the number of rows and columns of our subplot grid. For example, if we want to create a 2x2 grid of subplots, we would use:

```python
fig, axs = plt.subplots(2, 2)
```

This will create a figure object (fig) containing a 2x2 grid of subplots, and an array of axes objects (axs) corresponding to each subplot.

3. Set Labels on Individual Subplots
To set labels on individual subplots, we simply access the desired axes object (e.g., axs[0,0]) and call the set_xlabel() and set_ylabel() functions:

```python
axs[0,0].set_xlabel('X Label')
axs[0,0].set_ylabel('Y Label')
```

We can repeat this step for each subplot in our grid.

4. Add Common Labels
To add a common label for all subplots, we can use the fig.add_subplot() function which allows us to add an additional axes object to our figure. We then use this axes object to set the common label using set_xlabel() or set_ylabel().

```python
fig.add_subplot(111, frameon=False)
plt.tick_params(labelcolor='none', top='off', bottom='off', left='off', right='off')
plt.grid(False)
plt.xlabel('Common X Label')
plt.ylabel('Common Y Label')
```

Here, we are adding an empty subplot with three arguments: the number of rows, the number of columns, and the subplot index (in this case, '111' indicates a single subplot that spans the entire figure). We also turn off the frame and grid, and set the label colors to 'none' to create a blank axes object. Finally, we set the common labels using set_xlabel() and set_ylabel(). 

Now we have successfully added common axes labels to our subplots using Python!
