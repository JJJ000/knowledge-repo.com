---
title: Add labels containing values on pandas bar charts
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Use the `ax.text()` function to add text annotations to each bar of a Pandas bar plot, specifying the x and y coordinates, and the value to be displayed.
---

**Contents**

[TOC]

Section 1: Understanding the Problem
- The problem is to annotate bars with their respective values on Pandas bar plots in Python.
- Pandas bar plots are an effective way to visualize categorical data using rectangular bars with heights proportional to the values they represent.
- However, adding the actual values of these bars can make the plot more informative and insightful.

Section 2: Creating the Bar Plot
1. First, we need to import the required libraries: pandas and matplotlib.
2. Next, we need to create a sample dataset using pandas. For example: 
   data = {'apples': 10, 'oranges': 15, 'lemons': 5, 'limes': 20}
   df = pd.DataFrame(data, index=[0])
3. Now, we can plot the bar chart using matplotlib functionality that comes with pandas:
   df.plot(kind='bar')
   plt.show()

Section 3: Adding Annotations
1. We can use a for loop and the text method of matplotlib to annotate each bar. 
2. The text method takes three arguments - the x coordinate, the y coordinate and the label text.
3. We can access the values of each bar using the iteritems method of pandas dataframe object.
4. Using these values in the text method, we can add annotations to each bar.

For example: 

for index, value in df.iteritems():
   plt.text(index, value, str(value))

This code snippet iterates over each column in the dataframe, gets the value of each bar and adds a text label over it.

Section 4: Final Code
The final code will look something like this:

import pandas as pd
import matplotlib.pyplot as plt

data = {'apples': 10, 'oranges': 15, 'lemons': 5, 'limes': 20}
df = pd.DataFrame(data, index=[0])

ax = df.plot(kind='bar')
for index, value in df.iteritems():
    plt.text(index, value, str(value))

plt.show()

This will create a bar plot with annotations for each bar.
