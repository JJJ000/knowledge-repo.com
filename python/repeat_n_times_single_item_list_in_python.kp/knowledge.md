---
title: Make a list containing n repetitions of a single item
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Create a list of N copies of the same item using the [item] * N syntax.
---

**Contents**

[TOC]

**Section 1: Using a For Loop**

```python
# Create a list of single item repeated N times
N = 5
item = "Apple"

# Create an empty list
repeated_list = []

# Use a for loop to add the item to the list N times
for i in range(N):
    repeated_list.append(item)

# Print the list
print(repeated_list)

# Output: ['Apple', 'Apple', 'Apple', 'Apple', 'Apple']
```

**Section 2: Using List Comprehension**

```python
# Create a list of single item repeated N times
N = 5
item = "Apple"

# Use list comprehension to generate the list
repeated_list = [item for i in range(N)]

# Print the list
print(repeated_list)

# Output: ['Apple', 'Apple', 'Apple', 'Apple', 'Apple']
```

**Section 3: Using * Operator**

```python
# Create a list of single item repeated N times
N = 5
item = "Apple"

# Use the * operator to generate the list
repeated_list = [item] * N

# Print the list
print(repeated_list)

# Output: ['Apple', 'Apple', 'Apple', 'Apple', 'Apple']
```

**Section 4: Using itertools.repeat() Method**

```python
# Import itertools
import itertools

# Create a list of single item repeated N times
N = 5
item = "Apple"

# Use itertools.repeat() to generate the list
repeated_list = list(itertools.repeat(item, N))

# Print the list
print(repeated_list)

# Output: ['Apple', 'Apple', 'Apple', 'Apple', 'Apple']
```
