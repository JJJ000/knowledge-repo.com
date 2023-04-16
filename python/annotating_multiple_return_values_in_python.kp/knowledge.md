---
title: What is the process for labeling the data types of multiple return values?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: In Python, multiple return values can be annotated by using the typing.Tuple type annotation.
---

**Contents**

[TOC]

# 1. Using Tuple
A tuple can be used to annotate multiple return values in Python. This is done by declaring the tuple as the return type and enclosing the individual return values in parentheses.

```Python
def func() -> tuple:
    return (value1, value2)
```

# 2. Using NamedTuple
NamedTuple is a type of tuple that allows the individual return values to be assigned a name. This makes the code more readable and easier to maintain.

```Python
from collections import namedtuple

def func() -> namedtuple:
    return namedtuple('Values', ['value1', 'value2'])
```

# 3. Using TypedDict
TypedDict is a type of dictionary that allows the individual return values to be assigned a name and type. This makes the code more readable, easier to maintain, and allows for type checking.

```Python
from typing import TypedDict

def func() -> TypedDict:
    return TypedDict('Values', {'value1': int, 'value2': str})
```

# 4. Using Union
Union allows multiple types to be declared as the return type. This can be used to annotate multiple return values in Python by declaring the individual return values as different types.

```Python
from typing import Union

def func() -> Union[int, str]:
    return value1, value2
```
