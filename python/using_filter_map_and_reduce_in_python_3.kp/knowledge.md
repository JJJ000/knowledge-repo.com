---
title: What are the uses of filter, map, and reduce in Python 3?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Filter, map, and reduce can be used to iterate through a sequence in Python 3 and perform a specific operation on each element of the sequence, such as filtering out certain elements, mapping them to a new value, or reducing them to a single value.
---

**Contents**

[TOC]

### Filter

Filter is used to filter out elements from a sequence (list, tuple, dictionary, etc) based on a certain condition. It takes two arguments, a function and a sequence. The function returns a boolean value (True or False) and the sequence is filtered to only include elements for which the function returns True.

Syntax:

```
filtered_sequence = filter(function, sequence)
```

Example:

```
# filter out only even numbers
numbers = [1, 2, 3, 4, 5, 6]

def is_even(x):
    return x % 2 == 0

even_numbers = filter(is_even, numbers)

# even_numbers = [2, 4, 6]
```

### Map

Map is used to apply a function to all the elements of a sequence (list, tuple, dictionary, etc). It takes two arguments, a function and a sequence. The function is applied to each element of the sequence and a new sequence is returned with the modified elements.

Syntax:

```
mapped_sequence = map(function, sequence)
```

Example:

```
# add 1 to each element in the list
numbers = [1, 2, 3, 4, 5]

def add_one(x):
    return x + 1

new_numbers = map(add_one, numbers)

# new_numbers = [2, 3, 4, 5, 6]
```

### Reduce

Reduce is used to apply a function to all the elements of a sequence (list, tuple, dictionary, etc) and reduce it to a single value. It takes two arguments, a function and a sequence. The function is applied to each element of the sequence and the result is accumulated to a single value.

Syntax:

```
reduced_value = reduce(function, sequence)
```

Example:

```
# sum all the elements in the list
numbers = [1, 2, 3, 4, 5]

def add(x, y):
    return x + y

total = reduce(add, numbers)

# total = 15
```
