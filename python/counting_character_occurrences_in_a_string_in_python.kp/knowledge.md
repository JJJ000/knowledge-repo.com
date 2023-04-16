---
title: Determine how many times a character appears in a string
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the string method .count() to count the number of occurrences of a character in a string in Python.
---

**Contents**

[TOC]

##### Using a for loop:

```python
def count_char(string, char):
  count = 0
  for c in string:
    if c == char:
      count += 1
  return count

count_char('Hello', 'l')  # 2
```

##### Using list comprehension:

```python
def count_char(string, char):
  return len([c for c in string if c == char])

count_char('Hello', 'l')  # 2
```

##### Using the count() method:

```python
def count_char(string, char):
  return string.count(char)

count_char('Hello', 'l')  # 2
```

##### Using the collections module:

```python
from collections import Counter

def count_char(string, char):
  return Counter(string)[char]

count_char('Hello', 'l')  # 2
```
