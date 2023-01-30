---
title: What is the procedure for altering the font size on a matplotlib graph?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Set the `fontsize` parameter when calling the `set\_xlabel()` or `set\_ylabel()` methods.
---

**Contents**

[TOC]

1. **Import Libraries**
   ```python
   import matplotlib.pyplot as plt
   ```
2. **Create Plot**
   ```python
   plt.plot(x, y)
   ```
3. **Change Font Size**
   ```python
   plt.rcParams.update({'font.size': 18})
   ```
4. **Show Plot**
   ```python
   plt.show()
   ```
