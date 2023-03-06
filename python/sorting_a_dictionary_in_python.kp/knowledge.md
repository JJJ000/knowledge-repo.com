---
title: How can I iterate through a dictionary in python, where the keys are arranged in a sorted manner?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the `sorted()` function to sort the keys of the dictionary and iterate over them using a `for` loop.
---

**Contents**

[TOC]

## Obtaining Sorted Key List
First, we need to obtain a sorted list of keys from the dictionary. We can use the `sorted()` function to do this. Here's an example:

```python
my_dict = {'one': 1, 'three': 3, 'four': 4, 'two': 2}

sorted_keys = sorted(my_dict.keys())

print(sorted_keys) # output: ['four', 'one', 'three', 'two']
```

## Iterating Over Sorted Keys
Once we have a sorted list of keys, we can iterate over the dictionary using a `for` loop. Here's an example:

```python
for key in sorted_keys:
    print(key, my_dict[key])
```

This will output:

```
four 4
one 1
three 3
two 2
```

## Putting it all together
We can combine the two steps above into one concise piece of code:

```python
my_dict = {'one': 1, 'three': 3, 'four': 4, 'two': 2}

for key in sorted(my_dict.keys()):
    print(key, my_dict[key])
```

This will output:

```
four 4
one 1
three 3
two 2
```

So this is how you can iterate over a dictionary in sorted key order.
