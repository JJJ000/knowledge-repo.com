---
title: Randomly rearranging a collection of items
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: To shuffle a list of objects in Python, use the random.shuffle() function.
---

**Contents**

[TOC]

# Section 1: Using the Shuffle Function from the Random Module
Python provides a shuffle function from the random module. This function takes a list as an argument and shuffles it in place.

```
import random

my_list = [1,2,3,4,5]

random.shuffle(my_list)

print(my_list)

# Output: [4, 2, 5, 1, 3]
```

# Section 2: Using the Sample Function from the Random Module
The sample function from the random module also takes a list as an argument and returns a shuffled version of the list.

```
import random

my_list = [1,2,3,4,5]

shuffled_list = random.sample(my_list, len(my_list))

print(shuffled_list)

# Output: [4, 5, 2, 3, 1]
```

# Section 3: Using the Sorted Function with the Reverse Parameter
The sorted function takes a list as an argument and returns a sorted version of the list. By adding the reverse parameter, the list can be shuffled.

```
my_list = [1,2,3,4,5]

shuffled_list = sorted(my_list, reverse=True)

print(shuffled_list)

# Output: [5, 4, 3, 2, 1]
```

# Section 4: Using a For Loop
A for loop can be used to iterate over the list and append each item to a new list in a random order.

```
import random

my_list = [1,2,3,4,5]

shuffled_list = []

while len(my_list) > 0:
    index = random.randint(0, len(my_list)-1)
    shuffled_list.append(my_list[index])
    del my_list[index]

print(shuffled_list)

# Output: [3, 4, 1, 5, 2]
```
