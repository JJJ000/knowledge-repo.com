---
title: What is the best way to pick a random item from a list?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: You can use the random.choice() function to randomly select an item from a list in Python.
---

**Contents**

[TOC]

### Using Random Module
The `random` module can be used to select a random item from a list.

#### Syntax
The syntax for selecting a random item from a list is as follows: 

`random.choice(list_name)`

#### Example

For example, if we have a list of fruits:

```
fruits = ["apple", "banana", "cherry", "mango"]
```

We can select a random item from the list using the `random.choice()` function:

```
import random

random_fruit = random.choice(fruits)
print(random_fruit)
```

The output of the above code will be a random fruit from the list.

### Using Numpy
The `numpy` module can also be used to select a random item from a list.

#### Syntax
The syntax for selecting a random item from a list is as follows: 

`numpy.random.choice(list_name)`

#### Example

For example, if we have a list of fruits:

```
fruits = ["apple", "banana", "cherry", "mango"]
```

We can select a random item from the list using the `numpy.random.choice()` function:

```
import numpy

random_fruit = numpy.random.choice(fruits)
print(random_fruit)
```

The output of the above code will be a random fruit from the list.
