---
title: What are the values of a Python enum class?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the `enum.\_\_members\_\_.values()` method to get all values from a Python enum class.
---

**Contents**

[TOC]

1. Using `__members__` Attribute 

The `__members__` attribute of the Enum class is a dictionary containing all the values of the Enum class. It can be used to get all the values of the Enum class.

Example:
```python
from enum import Enum

class Color(Enum):
   RED = 1
   BLUE = 2
   GREEN = 3

# Get all values from Color enum class
values = Color.__members__.values()

# Print all values
for value in values:
   print(value)

# Output
Color.RED
Color.BLUE
Color.GREEN
```

2. Using `__class__` Attribute 

The `__class__` attribute of an Enum member can be used to get all the values of the Enum class.

Example:
```python
from enum import Enum

class Color(Enum):
   RED = 1
   BLUE = 2
   GREEN = 3

# Get all values from Color enum class
values = Color.RED.__class__

# Print all values
for value in values:
   print(value)

# Output
Color.RED
Color.BLUE
Color.GREEN
```

3. Using `values()` Method 

The `values()` method of the Enum class can be used to get all the values of the Enum class.

Example:
```python
from enum import Enum

class Color(Enum):
   RED = 1
   BLUE = 2
   GREEN = 3

# Get all values from Color enum class
values = Color.values()

# Print all values
for value in values:
   print(value)

# Output
Color.RED
Color.BLUE
Color.GREEN
```

4. Using `_member_map_` Attribute 

The `_member_map_` attribute of the Enum class is a dictionary containing all the values of the Enum class. It can be used to get all the values of the Enum class.

Example:
```python
from enum import Enum

class Color(Enum):
   RED = 1
   BLUE = 2
   GREEN = 3

# Get all values from Color enum class
values = Color._member_map_.values()

# Print all values
for value in values:
   print(value)

# Output
Color.RED
Color.BLUE
Color.GREEN
```
