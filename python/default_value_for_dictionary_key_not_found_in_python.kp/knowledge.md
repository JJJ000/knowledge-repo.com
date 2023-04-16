---
title: If a dictionary key is not found, provide a default value
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: If a dictionary key is not available, the get() method can be used to return a default value.
---

**Contents**

[TOC]

**Option 1: Using the get() Method**

The `get()` method can be used to return a default value if the key is not available in the dictionary. This method takes two arguments: the key and the default value to be returned.

Example: 

```
my_dict = {'name': 'John', 'age': 26}

default_value = my_dict.get('height', 0)

print(default_value)
```

Output: 0

**Option 2: Using the setdefault() Method**

The `setdefault()` method can be used to return a default value if the key is not available in the dictionary. This method takes two arguments: the key and the default value to be returned.

Example: 

```
my_dict = {'name': 'John', 'age': 26}

default_value = my_dict.setdefault('height', 0)

print(default_value)
```

Output: 0

**Option 3: Using the Defaultdict Class**

The `defaultdict` class can be used to return a default value if the key is not available in the dictionary. This class takes one argument: the default value to be returned.

Example: 

```
from collections import defaultdict

my_dict = defaultdict(lambda: 0)
my_dict['name'] = 'John'
my_dict['age'] = 26

default_value = my_dict['height']

print(default_value)
```

Output: 0
