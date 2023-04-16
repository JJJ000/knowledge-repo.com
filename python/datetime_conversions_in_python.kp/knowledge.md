---
title: Transforming between datetime, timestamp and datetime64
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Pandas provides the to\_datetime, to\_timestamp, and to\_datetime64 methods to convert between datetime, Timestamp, and datetime64 objects.
---

**Contents**

[TOC]

# Converting from datetime to Timestamp

Python's `datetime` module provides a `datetime.timestamp()` method which can be used to convert a `datetime` object to a Unix timestamp. The Unix timestamp is the number of seconds that have elapsed since January 1, 1970.

```python
from datetime import datetime

dt = datetime.now()
ts = dt.timestamp()
print(ts)
```

# Converting from Timestamp to datetime

The `datetime.fromtimestamp()` method can be used to convert a Unix timestamp to a `datetime` object.

```python
from datetime import datetime

ts = 1597284545
dt = datetime.fromtimestamp(ts)
print(dt)
```

# Converting from datetime to datetime64

Python's `numpy` module provides a `numpy.datetime64` class which can be used to convert a `datetime` object to a `datetime64` object.

```python
import numpy as np
from datetime import datetime

dt = datetime.now()
dt64 = np.datetime64(dt)
print(dt64)
```

# Converting from datetime64 to datetime

The `datetime.fromtimestamp()` method can be used to convert a `datetime64` object to a `datetime` object.

```python
import numpy as np
from datetime import datetime

dt64 = np.datetime64('2020-08-17T12:00:00')
dt = datetime.fromtimestamp(dt64.astype('datetime64[s]').astype(int))
print(dt)
```
