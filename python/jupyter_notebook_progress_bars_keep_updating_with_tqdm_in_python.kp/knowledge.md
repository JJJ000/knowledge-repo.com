---
title: The progress bars in jupyter notebook are printed repeatedly by tqdm
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: It is possible that the tqdm function is called repeatedly in a loop or function, causing new progress bars to be printed.
---

**Contents**

[TOC]

Introduction
---

tqdm is a Python library that provides a progress bar which helps users to keep track of their code's progress. It is commonly used in Jupyter Notebooks to show the progress of long-running loops or functions. The progress bar acts as a visual indicator that displays how much of a task has been completed and how much time is left.

Problem Description
---

In Jupyter Notebook, running tqdm repeatedly can sometimes result in multiple progress bars being printed out instead of a single one. This problem can be frustrating and confusing as it makes it harder to track the progress of a loop or function.

Cause
---

The root cause of this issue is that tqdm stores the progress bar in memory and adds to it each time it is called. This means that if tqdm is called repeatedly, it will create new instances of the progress bar, even if a previous instance exists.

Solution
---

There are a few solutions to this problem:

1. Clear the previous progress bar before calling tqdm again by using the `tqdm.clear()` function. This will remove the previous progress bar from memory and ensure that only one progress bar is printed.

2. Update the same progress bar by using the `tqdm.update()` function instead of calling `tqdm()` multiple times. This will ensure that the progress bar is only printed once and that the progress is updated each time.

3. Use the `tqdm_notebook()` function instead of `tqdm()` when running code in Jupyter Notebook. This function is specifically designed for use in Jupyter Notebook and will automatically clear any previous progress bars before printing a new one.

Example
---

Here is an example code block that demonstrates how to use `tqdm_notebook()` to avoid printing multiple progress bars in Jupyter Notebook:

```
from tqdm.notebook import tqdm_notebook

for i in tqdm_notebook(range(10)):
    # do some work
```

In this example, the `tqdm_notebook()` function is used instead of `tqdm()` to ensure that only one progress bar is printed. The `range(10)` argument represents the number of iterations in the loop. 

Conclusion
---

tqdm is a very useful library for tracking the progress of code in Python. However, when using it in Jupyter Notebook, care must be taken to ensure that only one progress bar is printed. This can be achieved by either clearing the previous progress bar, updating the same progress bar or using the `tqdm_notebook()` function.
