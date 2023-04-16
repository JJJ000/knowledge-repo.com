---
title: What is the process for interpreting an iso 8601-formatted date?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can parse an ISO 8601-formatted date in Python using the datetime.fromisoformat() method.
---

**Contents**

[TOC]

### Using datetime.strptime
The `datetime.strptime` method can be used to parse an ISO 8601-formatted date in Python. This method takes two arguments: a string representing the date and the format of the date. The following example shows how to parse an ISO 8601-formatted date using `datetime.strptime`:

```python
from datetime import datetime

date_string = '2020-03-01T09:00:00Z'
date_format = '%Y-%m-%dT%H:%M:%SZ'
date = datetime.strptime(date_string, date_format)
print(date)
# 2020-03-01 09:00:00
```

### Using dateutil.parser
The `dateutil.parser` module can also be used to parse an ISO 8601-formatted date in Python. This module takes a single argument: a string representing the date. The following example shows how to parse an ISO 8601-formatted date using `dateutil.parser`:

```python
from dateutil.parser import parse

date_string = '2020-03-01T09:00:00Z'
date = parse(date_string)
print(date)
# 2020-03-01 09:00:00
```

### Using iso8601
The `iso8601` module can also be used to parse an ISO 8601-formatted date in Python. This module takes a single argument: a string representing the date. The following example shows how to parse an ISO 8601-formatted date using `iso8601`:

```python
import iso8601

date_string = '2020-03-01T09:00:00Z'
date = iso8601.parse_date(date_string)
print(date)
# 2020-03-01 09:00:00
```

### Using arrow
The `arrow` module can also be used to parse an ISO 8601-formatted date in Python. This module takes a single argument: a string representing the date. The following example shows how to parse an ISO 8601-formatted date using `arrow`:

```python
import arrow

date_string = '2020-03-01T09:00:00Z'
date = arrow.get(date_string)
print(date)
# 2020-03-01T09:00:00+00:00
```
