---
title: Returning the first item in a Python sequence, or none if the sequence is empty
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: return next(iter(iterable), None)
---

**Contents**

[TOC]

### Using `for` Loop

```python
for item in iterable:
    return item
```

### Using `next()`

```python
return next(iterable, None)
```

### Using `try`/`except`

```python
try:
    return next(iterable)
except StopIteration:
    return None
```

### Using List Unpacking

```python
return next(iterable, None) if iterable else None
```
