---
title: What steps can I take to prevent pandas from creating an index when saving a csv file?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the index=False parameter when calling the to\_csv() function.
---

**Contents**

[TOC]

#1 Setting the Index to False

One way to avoid pandas creating an index in a saved csv in Python is to set the index to False. This can be done by passing the parameter index=False to the to_csv() function.

For example:

```
df.to_csv('my_csv_file.csv', index=False)
```

#2 Setting the Index Name

Another way to avoid pandas creating an index in a saved csv in Python is to set the index name to None. This can be done by passing the parameter index_label=None to the to_csv() function.

For example:

```
df.to_csv('my_csv_file.csv', index_label=None)
```

#3 Setting the Header

A third way to avoid pandas creating an index in a saved csv in Python is to set the header to False. This can be done by passing the parameter header=False to the to_csv() function.

For example:

```
df.to_csv('my_csv_file.csv', header=False)
```

#4 Setting the Line Terminator

A fourth way to avoid pandas creating an index in a saved csv in Python is to set the line terminator to an empty string. This can be done by passing the parameter line_terminator='' to the to_csv() function.

For example:

```
df.to_csv('my_csv_file.csv', line_terminator='')
```
