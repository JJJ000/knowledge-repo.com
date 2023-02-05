---
title: How can you use Python to transform a timestamp in seconds since epoch to a "datetime" object?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the `datetime.datetime.fromtimestamp()` function to convert seconds since epoch to a `datetime` object.
---

**Contents**

[TOC]

### Importing Libraries 

The following libraries must be imported to convert seconds since epoch to a `datetime` object:

```python
import datetime
import time
```

### Converting Seconds to Datetime 

The following code can be used to convert seconds since epoch to a `datetime` object:

```python
epoch_time = 1546300800
dt = datetime.datetime.fromtimestamp(epoch_time)
```

### Formatting Date 

The `datetime` object can be formatted to a desired output using the `strftime()` method:

```python
formatted_date = dt.strftime('%Y-%m-%d %H:%M:%S')
```

### Output 

The output of the code will be a `datetime` object formatted to the desired output:

```
2019-01-01 00:00:00
```
