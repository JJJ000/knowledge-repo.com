---
title: How to transform a string into a datetime object?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-11 00:00:00
updated_at: 2023-01-11 00:00:00
tldr: Use the `datetime.datetime.strptime()` function to convert a string to a datetime object.
---

**Contents**

[TOC]

### Importing the Necessary Libraries 
```python
import datetime
```

### Creating the Datetime Object
```python
datetime_object = datetime.datetime.strptime("May 1 2023 12:01PM", "%b %d %Y %I:%M%p")
```

### Displaying the Datetime Object
```python
print(datetime_object)
```

### Output
```
2023-05-01 12:01:00
```
