---
title: Create random whole numbers between 0 and 9
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: You can generate random integers between 0 and 9 in Python using the function `randint(0, 9)`.
---

**Contents**

[TOC]

# Using the Random Module

The random module in Python is used to generate random numbers. To generate random integers between 0 and 9, the `randint()` function can be used.

```python
import random

# Generate a random integer between 0 and 9
random_int = random.randint(0, 9)
```

# Using the Numpy Module

The numpy module in Python can also be used to generate random integers between 0 and 9. The `random.randint()` function can be used to generate random integers between two given numbers.

```python
import numpy as np

# Generate a random integer between 0 and 9
random_int = np.random.randint(0, 9)
```

# Using the Random Function

The `random()` function can also be used to generate random integers between 0 and 9.

```python
import random

# Generate a random integer between 0 and 9
random_int = int(random.random() * 10)
```
