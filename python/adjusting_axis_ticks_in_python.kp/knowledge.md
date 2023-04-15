---
title: Altering the interval between tick marks on the x or y axis
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-30 00:00:00
updated_at: 2023-04-30 00:00:00
tldr: To change the tick frequency on an axis in Python, use the set\_xticks() or set\_yticks() methods.
---

**Contents**

[TOC]

**Section 1: Change Tick Frequency on X Axis**

1. Using Matplotlib:

The tick frequency on the x axis can be changed using the Matplotlib library. To do this, use the xticks() function and specify the desired frequency. For example, to set the x axis ticks to appear every 5 units, you would use the following code:

```
plt.xticks(np.arange(min(x), max(x)+1, 5))
```

2. Using Seaborn:

The tick frequency on the x axis can also be changed using the Seaborn library. To do this, use the set_xticks() function and specify the desired frequency. For example, to set the x axis ticks to appear every 5 units, you would use the following code:

```
sns.set_xticks(np.arange(min(x), max(x)+1, 5))
```

**Section 2: Change Tick Frequency on Y Axis**

1. Using Matplotlib:

The tick frequency on the y axis can be changed using the Matplotlib library. To do this, use the yticks() function and specify the desired frequency. For example, to set the y axis ticks to appear every 5 units, you would use the following code:

```
plt.yticks(np.arange(min(y), max(y)+1, 5))
```

2. Using Seaborn:

The tick frequency on the y axis can also be changed using the Seaborn library. To do this, use the set_yticks() function and specify the desired frequency. For example, to set the y axis ticks to appear every 5 units, you would use the following code:

```
sns.set_yticks(np.arange(min(y), max(y)+1, 5))
```
