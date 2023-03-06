---
title: Rotating the text on labels in seaborn factorplot
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: To rotate label text in seaborn factorplot in Python, use the `rotate` parameter with the desired angle value in the `xticklabels` parameter.
---

**Contents**

[TOC]

Introduction
Seaborn is a powerful visualization library in Python, which provides a high-level interface for creating informative statistical graphics. One of the commonly used plots in Seaborn is factorplot, which is used to visualize categorical data. In factorplot, we can show the relationship between two categorical variables using different plot types. However, sometimes we need to rotate the label text in the factorplot to improve its readability. In this tutorial, we will see how to rotate the label text in Seaborn factorplot using Python.

Steps to Rotate Label Text in Seaborn Factorplot

Step 1: Import the necessary libraries
To create a Seaborn factorplot and rotate the label text, we first need to import the necessary libraries:

```
import seaborn as sns
import matplotlib.pyplot as plt
```

Step 2: Load the dataset
We will load the dataset used for creating the factorplot. For this tutorial, we will use the 'tips' dataset, which is available in seaborn's built-in datasets.

```
tips = sns.load_dataset('tips')
```

Step 3: Create a factorplot
We will create a factorplot using the 'sns.factorplot' function. We will set the 'x' and 'y' parameters to the categorical columns from the 'tips' dataset. Then, we will set the 'kind' parameter to the type of plot we want to create. For this tutorial, we will use the 'bar' plot.

```
sns.factorplot(x='day', y='total_bill', data=tips, kind='bar')
```

Step 4: Rotate the label text
To rotate the label text, we will use the 'set_xticklabels' function of the axes object. We will set the 'rotation' parameter to the angle at which we want to rotate the label text. For this tutorial, we will set it to 45 degrees.

```
ax = sns.factorplot(x='day', y='total_bill', data=tips, kind='bar')
ax.set_xticklabels(rotation=45)
```

Conclusion
In this tutorial, we saw how to rotate the label text in Seaborn factorplot using Python. We used the 'set_xticklabels' function of the axes object to rotate the label text. By adjusting the angle of rotation, we can improve the readability of the plot and make it more informative.
