---
title: What is the syntax for converting an iso 8601 datetime string into a Python datetime object?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the datetime.fromisoformat() method to translate an ISO 8601 datetime string into a Python datetime object.
---

**Contents**

[TOC]

**Section 1: Import the necessary library**

```python
from datetime import datetime
```

**Section 2: Parse the ISO 8601 string**

```python
date_string = '2020-04-01T13:30:00'
date_object = datetime.strptime(date_string, '%Y-%m-%dT%H:%M:%S')
```

**Section 3: Print the result**

```python
print(date_object)
```

**Section 4: Output**

```
2020-04-01 13:30:00
```
