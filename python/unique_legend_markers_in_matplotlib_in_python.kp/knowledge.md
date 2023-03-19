---
title: How to display matplotlib's legend markers only a single time?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: To add legend markers only once in Matplotlib, you can use the handle variable returned by the plot function to specify the corresponding marker in the legend.
---

**Contents**

[TOC]

Section 1: Introduction
Matplotlib is a popular data visualization library in Python. Legends are an essential part of creating interactive plots using Matplotlib. However, legend markers can repeat if there are multiple items with the same label. This can make the legend look cluttered, and it may become difficult to interpret. In this article, we will discuss how to show legend markers only once in Python.

Section 2: The Problem of Repeating Markers in Legends
The default behavior of Matplotlib is to repeat markers in the legend if there are multiple items with the same label. This is because the legend is meant to identify different lines that may be plotted on the same graph. Each line has its own marker or line style associated with it. If you have multiple lines with the same label, Matplotlib will not differentiate them and will repeat the marker for each line. This can create a lot of clutter in the legend.

Section 3: Solving the Problem of Repeating Markers in Legends
One way to solve the problem of repeating markers in legends is to create a custom legend handler using the Line2D object. This handler allows you to specify the number and style of markers that should be displayed in the legend. You can use the Line2D object to define a custom line style for each item in the plot. Then, you can use the legend handler to display the line style in the legend only once, even if there are multiple items with the same label. 

Section 4: Conclusion
In conclusion, legends are an essential part of creating interactive plots using Matplotlib. However, legend markers can quickly become cluttered if there are multiple items with the same label. By creating a custom legend handler using the Line2D object, you can display legend markers only once, making it easier to interpret the legend.
