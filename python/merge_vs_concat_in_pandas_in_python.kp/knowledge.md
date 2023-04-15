---
title: How do merge() and concat() in pandas differ from each other?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The merge() function is used to combine rows based on one or more common columns, while the concat() function is used to combine multiple dataframes along a particular axis.
---

**Contents**

[TOC]

## Introduction 
Pandas is one of the most widely used data manipulation libraries in the field of data science. It provides many functions for data manipulation and analysis, among which, `merge()` and `concat()` are two of the most important ones that are used frequently. Both `merge()` and `concat()` are used for combining data frames in pandas. However, there are some differences between the two functions that we will discuss in the following sections of this article.

## Concat()

- Combines multiple data frames into a single data frame.
- The data frames can either be stacked vertically or horizontally.
- The axis parameter can be passed either 0 or 1, for vertical or horizontal concatenation, respectively.
- Column names don't have to be identical across data frames.
- Fills missing values with NaN.


## Merge()

- Combines two data frames into a single data frame based on a specified column(s).
- Can be used for various types of joins such as inner, outer, left and right.
- Can handle overlapping column names by suffixing them.
- Does not fill missing values.


## Which one to use?

- Use `concat()` when combining data frames with identical columns, and simple stacking is required, such as stacking data frames vertically or horizontally.
- Use `merge()` when combining data frames with different columns or when performing complex joining operations based on common columns. 


## Conclusion

In summary, both `merge()` and `concat()` are useful functions in pandas for combining data frames. Both have their own uses, and the choice of which one to use depends on the specific needs of the analysis. `Merge()` is more suited to handle complex joining operations based on common columns, while `concat()` is better suited for simple stacking of data frames.
