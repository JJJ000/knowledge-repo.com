---
title: What steps are necessary to eliminate the top and right axis in matplotlib?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: To remove the top and right axis in matplotlib in Python, use the command `spines().top.set\_visible(False)`, `spines().right.set\_visible(False)`.
---

**Contents**

[TOC]

Section 1: Importing Libraries 
```python
import matplotlib.pyplot as plt
```
Firstly, you need to import the Matplotlib library in Python to work with the plotting, visualization, and graphical representation of data. 

Section 2: Creating the Plot
```python
fig, ax = plt.subplots()
```
In this section, you can create the plot by using the subplots() method of Matplotlib. Here fig stores the reference to the figure and ax stores the reference to the axes.

Section 3: Removing the Top and Right Axis
```python
ax.spines['top'].set_visible(False)
ax.spines['right'].set_visible(False)
```
Once the plot is created, you can remove the top and right axis by setting their visibility status to False using the spines attribute.

Section 4: Displaying the Plot 
```python
plt.show()
```
Finally, you can display the plot by using the show() method of Matplotlib. 

Putting it all together, the code will look like this:
```python
import matplotlib.pyplot as plt

# Create the plot
fig, ax = plt.subplots()

# Remove the top and right axis
ax.spines['top'].set_visible(False)
ax.spines['right'].set_visible(False)

# Display the plot
plt.show()
```
