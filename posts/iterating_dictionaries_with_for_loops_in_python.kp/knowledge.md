---
title: Looping through dictionaries using 'for' statements
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-08 00:00:00
updated_at: 2023-01-08 00:00:00
tldr: For each key-value pair in the dictionary, the 'for' loop can be used to iterate over the keys, values, or both.
---

**Contents**

[TOC]

### Iterating over Dictionary Keys

We can use a `for` loop to iterate over the keys of a dictionary. 

```python
my_dict = {'a': 1, 'b': 2, 'c': 3}

for key in my_dict:
    print(key)
```

This will print out:
```python
a
b
c
```

### Iterating over Dictionary Values

We can also use a `for` loop to iterate over the values of a dictionary. 

```python
my_dict = {'a': 1, 'b': 2, 'c': 3}

for value in my_dict.values():
    print(value)
```

This will print out:
```python
1
2
3
```

### Iterating over Dictionary Items

We can also use a `for` loop to iterate over the items (key, value pairs) of a dictionary. 

```python
my_dict = {'a': 1, 'b': 2, 'c': 3}

for key, value in my_dict.items():
    print(key, value)
```

This will print out:
```python
a 1
b 2
c 3
```
