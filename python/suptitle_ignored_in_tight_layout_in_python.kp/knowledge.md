---
title: The function tight_layout() doesn't consider the figure's suptitle
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: True, tight\_layout() doesn`t take into account figure suptitle in Python.
---

**Contents**

[TOC]

# Introduction
When plotting figures in Python, it is common to use `tight_layout()` to adjust the spacing between subplots and make the figure look more appealing. However, it seems that `tight_layout()` does not take into account the figure `suptitle` which is used to add a centered title above the figure. Let's explore this issue further in the following sections.

# Example
We can start by creating a simple figure with a suptitle and two subplots using the following code:

```python
import matplotlib.pyplot as plt

fig, (ax1, ax2) = plt.subplots(nrows=2, figsize=(6, 6))
fig.suptitle("Figure Suptitle")
ax1.plot([1, 2, 3], [1, 2, 3])
ax2.plot([1, 2, 3], [3, 2, 1])
plt.tight_layout()
plt.show()
```

The resulting figure looks like this:

![figure](https://imgur.com/knV7HJK.png)

As we can see, the suptitle is outside of the figure boundary, indicating that `tight_layout()` did not adjust the spacing correctly.

# Explanation

The reason for this behavior is that `tight_layout()` calculates the spacing based on the subplots and their contents, but it does not take into account any additional elements outside of the subplots such as axis labels, titles, legends, or suptitles. Thus, when we add a suptitle, it expands the overall size of the figure but `tight_layout()` is not aware of this change and does not adjust the spacing accordingly.

# Solution
One solution to this problem is to use the `subplots_adjust()` method instead of `tight_layout()`. This method allows us to manually adjust the spacing between subplots and other figure elements. For example, we can add the following code after creating the subplots to adjust the top and bottom margins of the figure:

```python
fig.subplots_adjust(top=0.90, bottom=0.10)
```

This will move the subplots closer to the top of the figure and leave more space at the bottom for the suptitle. The resulting figure looks like this:

```python
import matplotlib.pyplot as plt

fig, (ax1, ax2) = plt.subplots(nrows=2, figsize=(6, 6))
fig.suptitle("Figure Suptitle")
ax1.plot([1, 2, 3], [1, 2, 3])
ax2.plot([1, 2, 3], [3, 2, 1])
fig.subplots_adjust(top=0.90, bottom=0.10)
plt.show()
```

![figure](https://imgur.com/xoq3i8h.png)

As we can see, the suptitle is now within the figure boundary and the spacing between the subplots is still adjusted.

# Conclusion
In summary, `tight_layout()` does not take into account figure elements outside of the subplots such as suptitles. To adjust the spacing correctly in this case, we can use the `subplots_adjust()` method to manually adjust the margins of the figure.
