---
title: What is the key with the highest value in the dictionary?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The key with the maximum value in a dictionary can be obtained using the max() function.
---

**Contents**

[TOC]

#### Solution 1: 
Using the `max()` function:

```python
d = {'a':1, 'b':2, 'c':3}

# Get the key corresponding to the maximum value
key_max = max(d, key=d.get)

print(key_max) # Output: c
```

#### Solution 2: 
Using the `max()` and `dict.items()` functions:

```python
d = {'a':1, 'b':2, 'c':3}

# Get the key corresponding to the maximum value
key_max = max(d.items(), key=lambda x: x[1])[0]

print(key_max) # Output: c
```

#### Solution 3: 
Using a `for` loop:

```python
d = {'a':1, 'b':2, 'c':3}

# Initialize the maximum value and corresponding key
max_value = float('-inf')
key_max = None

# Iterate through the dictionary
for k, v in d.items():
    # Check if the value is greater than the current maximum
    if v > max_value:
        # Update the maximum value and corresponding key
        max_value = v
        key_max = k

print(key_max) # Output: c
```

#### Solution 4: 
Using the `max()` and `dict.keys()` functions:

```python
d = {'a':1, 'b':2, 'c':3}

# Get the key corresponding to the maximum value
key_max = max(d.keys(), key=(lambda k: d[k]))

print(key_max) # Output: c
```
