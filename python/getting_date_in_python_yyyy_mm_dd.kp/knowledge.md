---
title: How to obtain the current date in yyyy-mm-dd format using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-30 00:00:00
updated_at: 2023-04-30 00:00:00
tldr: Today`s date in YYYY-MM-DD format can be obtained using the datetime.date.today() function.
---

**Contents**

[TOC]

# Using datetime library

The `datetime` library in Python can be used to easily get the current date.

```python
import datetime

today = datetime.date.today()

print(today.strftime('%Y-%m-%d'))
```

# Using time library

The `time` library in Python can also be used to get the current date.

```python
import time

today = time.strftime('%Y-%m-%d')

print(today)
```
