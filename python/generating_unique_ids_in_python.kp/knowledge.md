---
title: In python, what is the method of generating a distinctive identification?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Use the UUID library in Python to generate a unique ID.
---

**Contents**

[TOC]

### Using the uuid module

One way to generate a unique ID in Python is to use the built-in uuid module. This module provides various functions to generate UUIDs (Universally Unique Identifiers) that are unique across time and space. Here's an example:

```python
import uuid

unique_id = uuid.uuid4()

print(unique_id)
```

The `uuid.uuid4()` function generates a random UUID. The resulting UUID is a 128-bit integer, represented as a string of 32 hexadecimal digits, separated by hyphens in standard UUID format.

### Using the time and random modules

Another way to generate a unique ID is to combine the current time and a random number. Here's an example:

```python
import time
import random

def generate_unique_id():
    timestamp = int(time.time() * 1000)  # milliseconds since epoch
    rand_num = random.randint(0, 1000000)
    unique_id = f"{timestamp}-{rand_num}"
    return unique_id

print(generate_unique_id())
```

This function generates a string that combines the current timestamp (in milliseconds since epoch) and a random number between 0 and 1 million. This method is less reliable than using UUIDs because it has a higher chance of collisions, but it can still serve as a simple and quick solution for generating unique IDs.

### Using a counter

If you're generating a sequence of IDs and don't necessarily need them to be globally unique, you could use a counter to generate unique numbers. Here's an example:

```python
class IDGenerator:
    def __init__(self):
        self.counter = 0

    def generate_id(self):
        self.counter += 1
        return self.counter

id_gen = IDGenerator()
print(id_gen.generate_id())
```

This class maintains a counter that starts at 0 and increments every time the `generate_id()` method is called. This method returns the current value of the counter as the unique ID. Note that this approach only generates unique IDs within the context of the IDGenerator instance, so if you create multiple instances of the class, they will each have their own separate counters.
