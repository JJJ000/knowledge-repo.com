---
title: Iterate over a list in reverse order in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: To traverse a list in reverse order in Python, use the built-in reversed() function.
---

**Contents**

[TOC]

**Solution 1: Using a for loop**

```python
# Initialize the list
my_list = [1, 2, 3, 4, 5]

# Traverse the list in reverse order
for i in range(len(my_list)-1, -1, -1):
    print(my_list[i])
```

**Solution 2: Using a while loop**

```python
# Initialize the list
my_list = [1, 2, 3, 4, 5]

# Initialize the counter
i = len(my_list) - 1

# Traverse the list in reverse order
while i >= 0:
    print(my_list[i])
    i -= 1
```

**Solution 3: Using reversed()**

```python
# Initialize the list
my_list = [1, 2, 3, 4, 5]

# Traverse the list in reverse order
for i in reversed(my_list):
    print(i)
```

**Solution 4: Using slicing**

```python
# Initialize the list
my_list = [1, 2, 3, 4, 5]

# Traverse the list in reverse order
for i in my_list[::-1]:
    print(i)
```
