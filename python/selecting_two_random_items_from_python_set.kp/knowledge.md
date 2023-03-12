---
title: What would be the process of selecting 2 random elements from a Python set?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Convert the set to a list and use the random.sample() function with a sample size of 2.
---

**Contents**

[TOC]

# Section 1: Converting Set to List

Since sets in Python are unordered, there is no straightforward way to pick random items from a set. One simple solution is to convert the set into a list and then pick random items from the list.

```python
my_set = {1, 2, 3, 4, 5}
my_list = list(my_set)
```

# Section 2: Using random.sample()

The random module in Python provides the sample() function that can be used to pick random items from a list.

```python
import random
my_set = {1, 2, 3, 4, 5}
my_list = list(my_set)
random_items = random.sample(my_list, 2)
```

In this example, we pass the list and the number of items we want to pick as arguments to the sample() function. The function returns a list of randomly selected items.

# Section 3: Using set.pop()

Another solution to pick random items from a set is to use the pop() method of the set. The pop() method removes a random item from the set and returns it.

```python
my_set = {1, 2, 3, 4, 5}
random_item1 = my_set.pop()
random_item2 = my_set.pop()
```

In this example, we call the pop() method twice on the set to get two random items. Note that since sets are unordered, there is no guarantee which items will be picked.

# Section 4: Combining Solutions

We can also combine the solutions to convert the set into a list and then use the sample() function to get random items.

```python
import random
my_set = {1, 2, 3, 4, 5}
my_list = list(my_set)
random_items = random.sample(my_list, 2)
```

This solution gives us more control over which items we want to pick and ensures that we get the correct number of items.
