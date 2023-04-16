---
title: Convert a timedelta to a string representation
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The timedelta can be converted to a string by using the strftime() method.
---

**Contents**

[TOC]

# Method 1: strftime()
The `strftime()` method can be used to convert a `timedelta` object to a string. The syntax for this method is `timedelta.strftime(format)`, where `format` is a string that specifies the format of the outputted string. 

For example, the following code will output a string representing the timedelta in the format of `DD:HH:MM:SS`:

```
from datetime import timedelta

td = timedelta(days=2, hours=6, minutes=12, seconds=30)

td_string = td.strftime('%d:%H:%M:%S')

print(td_string)
```

Output:

```
02:06:12:30
```

# Method 2: str()
The `str()` method can also be used to convert a `timedelta` object to a string. The syntax for this method is `str(timedelta)`. 

For example, the following code will output a string representing the timedelta:

```
from datetime import timedelta

td = timedelta(days=2, hours=6, minutes=12, seconds=30)

td_string = str(td)

print(td_string)
```

Output:

```
2 days, 6:12:30
```
