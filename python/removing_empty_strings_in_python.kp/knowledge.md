---
title: Delete any blank strings from a list of strings
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: list = [x for x in list if x != ``]
---

**Contents**

[TOC]

### Using List Comprehension

```python
filtered_list = [string for string in list_of_strings if string]
```

### Using Filter Function

```python
filtered_list = list(filter(None, list_of_strings))
```

### Using For Loop

```python
filtered_list = []
for string in list_of_strings:
    if string:
        filtered_list.append(string)
```

### Using While Loop

```python
filtered_list = []
i = 0
while i < len(list_of_strings):
    if list_of_strings[i]:
        filtered_list.append(list_of_strings[i])
    i += 1
```
