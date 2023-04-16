---
title: Decrease the font size of matplotlib tick labels
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To make tick labels font size smaller in Matplotlib, set the fontsize parameter of the xticks() or yticks() function.
---

**Contents**

[TOC]

**Section 1: Importing Necessary Modules**

```python
import matplotlib.pyplot as plt
```

**Section 2: Setting the Font Size for Tick Labels**

```python
ax = plt.gca()
ax.tick_params(axis='both', which='major', labelsize=8)
```

**Section 3: Plotting the Graph**

```python
plt.plot([1,2,3,4])
plt.show()
```

**Section 4: Saving the Graph**

```python
plt.savefig('my_graph.png')
```
