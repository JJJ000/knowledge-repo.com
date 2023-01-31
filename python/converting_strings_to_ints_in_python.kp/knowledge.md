---
title: Change all string elements in a list to integers
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Use the list comprehension syntax [int(x) for x in list] to convert all strings in a list to int in Python.
---

**Contents**

[TOC]

### Section 1: Using List Comprehension

The following code uses list comprehension to convert all strings in a list to int:

```
int_list = [int(x) for x in my_list]
```

Where `my_list` is the list of strings that need to be converted to integers.

### Section 2: Using Map

The following code uses the `map` function to convert all strings in a list to int:

```
int_list = list(map(int, my_list))
```

Where `my_list` is the list of strings that need to be converted to integers.

### Section 3: Using For Loop

The following code uses a for loop to convert all strings in a list to int:

```
int_list = []
for x in my_list:
    int_list.append(int(x))
```

Where `my_list` is the list of strings that need to be converted to integers.

### Section 4: Using While Loop

The following code uses a while loop to convert all strings in a list to int:

```
int_list = []
i = 0
while i < len(my_list):
    int_list.append(int(my_list[i]))
    i += 1
```

Where `my_list` is the list of strings that need to be converted to integers.
