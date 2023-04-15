---
title: What steps can be taken to incorporate hovering annotations on a plot?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Use the matplotlib`s `annotate` function to add hovering annotations to a plot in Python.
---

**Contents**

[TOC]

Section 1: Introduction
Python provides many visualization libraries that allow you to plot, display and analyze data quickly and conveniently. However, it can be difficult to have a comprehensive understanding of the plot without additional information. In this tutorial, we will learn how to create hovering annotations on a plot in Python.

Section 2: Setting up the Environment
The first step is to import the necessary libraries. We will use matplotlib and pandas libraries. Additionally, we will use the "mplcursors" library that allows adding annotations on matplotlib figures.

```
!pip install mplcursors
import pandas as pd
import matplotlib.pyplot as plt
import mplcursors
```

Section 3: Adding Annotations to the Plot
To add annotations to the plot, we first create a scatter plot using the pandas dataframe method "plot()". We can then define the data points that we want to annotate by defining the x and y coordinates individually.

We then create the mplcursors cursor object that will allow us to annotate specific data points on the plot. We do this by calling the "mplcursors.cursor()" function and then setting the "hover" and "annotate" attributes to True. We can also define the formatting of the annotation as well.

```
# Create DataFrame
df = pd.DataFrame({'x':[1,2,3,4,5], 'y':[2,4,6,8,10]})

# Create Scatter Plot
fig, ax = plt.subplots()
df.plot(kind='scatter', x='x', y='y', ax=ax)

# Define Annotations
annotations = [ax.annotate(f"({x}, {y})", (x, y), xytext=(0, 10),
                textcoords='offset pixels', ha='center')
             for x, y in zip(df['x'], df['y'])]

# Create mplcursors Cursor
cursor = mplcursors.cursor(hover=True)
cursor.connect("add", lambda sel: sel.annotation.set_text(
    f"({sel.target[0]:.2f}, {sel.target[1]:.2f})"))
cursor.connect("add", lambda sel: sel.annotation.get_bbox_patch().set_alpha(0.4))
```

Section 4: Displaying the Plot
Once we have created the plot with annotations, we can display it by calling the plt.show() function.

```
plt.show()
```

Conclusion
In this tutorial, we learned how to add hovering annotations to a plot in Python. The mplcursors library makes it easy to annotate specific data points with additional information. We hope that you find this tutorial useful for your data science and visualization projects.
