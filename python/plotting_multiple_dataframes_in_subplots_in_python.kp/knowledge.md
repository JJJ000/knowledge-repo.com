---
title: What is the process of creating subplots to display multiple dataframes simultaneously?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use matplotlib`s `subplots` function to create a grid of plots and plot each dataframe on a subplot using the `ax` parameter of each plot method.
---

**Contents**

[TOC]

## Section 1: Import Required Libraries

We need to import the necessary libraries to create subplots and plot the dataframes. Here, we will import the matplotlib library, which is a widely used library for data visualization in Python.

```python
import matplotlib.pyplot as plt
```

## Section 2: Create DataFrames

We can create multiple dataframes to be plotted in subplots. In this example, we will create two dataframes with different sets of data.

```python
import pandas as pd

# create first dataframe with some data
df1 = pd.DataFrame({
    'x': range(10),
    'y': range(10)
})

# create second dataframe with some other data
df2 = pd.DataFrame({
    'x': range(10),
    'y': [i**2 for i in range(10)]
})
```

## Section 3: Create Subplots and Plot DataFrames

Now, we can create subplots and plot the dataframes in them. Here, we create a figure with two subplots side-by-side.

```python
# create figure with two subplots side-by-side
fig, axs = plt.subplots(1, 2, figsize=(10, 5))

# plot first dataframe in the first subplot
axs[0].plot(df1['x'], df1['y'])
axs[0].set_title('Dataframe 1')

# plot second dataframe in the second subplot
axs[1].plot(df2['x'], df2['y'])
axs[1].set_title('Dataframe 2')

# set overall title for the figure
fig.suptitle('Two Dataframes in Subplots')
```

## Section 4: Show the Plots

Finally, we can show the plots by calling `plt.show()`.

```python
plt.show()
```
