---
title: What are the distinctions between iloc and loc?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: loc is used to access a group of rows and columns by label(s) or a boolean array, while iloc is used to access a group of rows and columns by integer position(s).
---

**Contents**

[TOC]

### Functionality

The primary difference between iloc and loc is the way they access data. iloc uses integer-based indexing while loc uses label-based indexing. 

### Syntax

iloc uses array-style indexing where you provide the index of the row and column you want to access. The syntax is `df.iloc[row_index, column_index]`.

loc uses label-based indexing where you provide the label of the row and column you want to access. The syntax for this is `df.loc[row_label, column_label]`.

### Performance

iloc is generally faster than loc since it uses integer-based indexing, which is more efficient than label-based indexing.

### Limitations

iloc cannot access data using labels, while loc can access data using labels as well as integers.
