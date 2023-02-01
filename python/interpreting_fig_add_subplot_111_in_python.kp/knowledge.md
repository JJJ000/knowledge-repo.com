---
title: What is the purpose of the argument fig.add_subplot(111) in a figure?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Fig.add\_subplot(111) is a command that creates a single subplot in a figure with 1 row, 1 column, and the 1st subplot.
---

**Contents**

[TOC]

# Section 1: What is fig.add_subplot?

fig.add_subplot() is a function in the matplotlib library of Python, used to create a subplot in a figure. It takes three parameters: nrows, ncols, and index.

# Section 2: What is nrows, ncols, and index?

nrows and ncols are the number of rows and columns of subplots in the figure. The index parameter is the index of the subplot in the figure, starting from the top left corner with an index of 1 and increasing by 1 with each row.

# Section 3: What does fig.add_subplot(111) mean?

fig.add_subplot(111) is a shorthand for fig.add_subplot(1, 1, 1). This means that the figure has one row, one column, and the first subplot is being created.
