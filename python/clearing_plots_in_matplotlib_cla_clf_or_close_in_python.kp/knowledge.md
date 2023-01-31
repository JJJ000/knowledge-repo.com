---
title: What are the functions to use to clear a plot in matplotlib?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Use cla() to clear an axes, clf() to clear the entire figure, and close() to close the figure window.
---

**Contents**

[TOC]

### cla()
`cla()` is used to clear the current axes. It sets the x and y limits to the default values and removes all lines, patches, and text objects from the axes. 

### clf()
`clf()` is used to clear the entire figure. It removes all axes, lines, patches, and text objects from the figure.

### close()
`close()` is used to close the current figure window. It closes the figure window and sets the current figure to `None`.
