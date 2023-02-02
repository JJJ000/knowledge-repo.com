---
title: When plotting a figure with pyplot on pycharm, a userwarning may appear indicating that matplotlib is using a non-gui backend, so the figure cannot be displayed
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: This warning can be safely ignored as it does not affect the plotting of the figure.
---

**Contents**

[TOC]

## Overview

When plotting a figure with pyplot on Pycharm in Python, the user may encounter the warning message "UserWarning: Matplotlib is currently using agg, which is a non-GUI backend, so cannot show the figure." This warning message indicates that the figure cannot be displayed due to the current backend being used by Matplotlib.

## What is Matplotlib?

Matplotlib is a Python library used for plotting data. It is capable of creating a variety of different types of plots, including line graphs, bar charts, histograms, and more. Matplotlib can be used in both the Python scripting language and in the IPython shell.

## What is a Backend?

A backend is the part of a computer program that interacts with the operating system and other programs. In the case of Matplotlib, the backend is responsible for rendering the plots to the screen or to a file. Matplotlib has several different backends, including the agg backend, which is the default backend used when plotting on Pycharm.

## What is the Agg Backend?

The agg backend is a non-GUI backend, meaning that it does not use a graphical user interface. This means that it cannot display the figure, which is why the user receives the warning message. To display the figure, the user must switch to a different backend, such as the TkAgg backend.
