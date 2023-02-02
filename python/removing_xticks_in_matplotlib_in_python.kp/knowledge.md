---
title: How do I get rid of the x-axis tick marks in a matplotlib plot?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: To remove xticks in a matplotlib plot, use plt.xticks([]) or plt.tick\_params(axis=`x`, which=`both`, bottom=False, top=False, labelbottom=False).
---

**Contents**

[TOC]

**1. Import the necessary libraries**

```python
import matplotlib.pyplot as plt
```

**2. Create a plot**

```python
plt.plot([1,2,3,4,5], [1,4,9,16,25])
```

**3. Remove the xticks**

```python
plt.xticks([])
```

**4. Show the plot**

```python
plt.show()
```
