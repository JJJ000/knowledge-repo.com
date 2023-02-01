---
title: What are the distinctions between the map, applymap and apply methods in pandas?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: The map method applies a function to each element of a series, the applymap method applies a function to each element of a DataFrame, and the apply method applies a function along an axis of a DataFrame.
---

**Contents**

[TOC]

### Map
The `map` method applies a function to each element of a Series. It is used to transform each element of a Series. The `map` method can be used with a dictionary, a function, or another Series.

### Applymap
The `applymap` method applies a function to each element of a DataFrame. It is used to transform each element of a DataFrame. The `applymap` method can be used with a function or a Series.

### Apply
The `apply` method applies a function to a row or column of a DataFrame. It is used to transform a row or column of a DataFrame. The `apply` method can be used with a function or a Series.

### Difference
The main difference between `map`, `applymap` and `apply` is the object they are applied to. `map` is applied to a Series, `applymap` is applied to a DataFrame, and `apply` is applied to either a row or column of a DataFrame.
