---
title: Examining two dictionaries to determine how many matching (key, value) pairs they contain
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The number of (key, value) pairs equal between two dictionaries can be determined by using the len() function on the set created by the intersection of the two dictionaries.
---

**Contents**

[TOC]

### Creating the Dictionaries

We can create two dictionaries to compare.

```python
dict1 = {'a':1, 'b':2, 'c':3}
dict2 = {'a':1, 'b':2, 'd':4}
```

### Comparing the Dictionaries

We can compare the two dictionaries to check how many (key, value) pairs are equal.

```python
equal_pairs = 0

for key, value in dict1.items():
    if key in dict2 and dict2[key] == value:
        equal_pairs += 1

print(equal_pairs) # prints 2
```

### Output

The output of the code is 2, which means that there are two (key, value) pairs that are equal between the two dictionaries.
