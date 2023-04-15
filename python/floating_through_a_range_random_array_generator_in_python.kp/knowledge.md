---
title: Create an array of floating-point numbers randomly generated within a specified range
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the numpy library to create a random array of floats between a specified range.
---

**Contents**

[TOC]

## Section 1: Importing necessary libraries

We need to import the `random` module to generate random numbers and `numpy` module to create an array with these random numbers.

```python
import random
import numpy as np
```

## Section 2: Defining Range and Size

Now, we need to define the range from which we want to generate our random values and the size of our array.

```python
start_range = 0.0
end_range = 1.0
array_size = 10
```

## Section 3: Creating Random Floats

We can use the `random.uniform()` function from the `random` module to generate random floats between a specified range. We can use a `list comprehension` to create an array of random floats with the specified range and size.

```python
random_floats = np.array([random.uniform(start_range, end_range) for _ in range(array_size)])
print(random_floats)
```

This will output an array of 10 random floats between 0.0 and 1.0.

## Section 4: Final Code

The final code will look like this:

```python
import random
import numpy as np

start_range = 0.0
end_range = 1.0
array_size = 10

random_floats = np.array([random.uniform(start_range, end_range) for _ in range(array_size)])
print(random_floats)
``` 

This code will generate an array of 10 random floats between 0.0 and 1.0, similar to this:

```python
array([0.7351, 0.7297, 0.4242, 0.8933, 0.0344, 0.5117, 0.6394, 0.9894, 0.3911, 0.6377])
```
