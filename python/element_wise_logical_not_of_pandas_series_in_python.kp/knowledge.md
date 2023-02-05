---
title: What is the element-wise logical not of a pandas series?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: You can obtain the element-wise logical NOT of a pandas Series by using the `~` operator.
---

**Contents**

[TOC]

## Using the `~` Operator

The `~` operator can be used to obtain the element-wise logical NOT of a pandas series. For example:

```python
import pandas as pd

s = pd.Series([True, False, True])

not_s = ~s
```

This will result in a new pandas series with the logical NOT of the original series:

```python
not_s

0    False
1     True
2    False
dtype: bool
```

## Using the `.apply()` Method

The `.apply()` method can also be used to obtain the element-wise logical NOT of a pandas series. For example:

```python
import pandas as pd

s = pd.Series([True, False, True])

not_s = s.apply(lambda x: not x)
```

This will result in a new pandas series with the logical NOT of the original series:

```python
not_s

0    False
1     True
2    False
dtype: bool
```
