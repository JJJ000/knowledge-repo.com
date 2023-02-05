---
title: A version of random.choice that takes into account weights
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: A weighted version of random.choice in Python is random.choices, which allows for weights to be assigned to each element in the sequence.
---

**Contents**

[TOC]

# Weighted Choice
Weighted random choice is a method of randomly selecting an item from a list, where each item is associated with a weight. The item with the highest weight has the highest probability of being selected.

# Algorithm
The algorithm for weighted choice is as follows:

1. Calculate the total sum of all weights.
2. Generate a random number in the range of 0 to the total sum.
3. Iterate through the list of items and subtract each item’s weight from the random number.
4. The item whose weight causes the random number to be less than or equal to zero is the selected item.

# Implementation
The following is a simple implementation of weighted choice in Python:

```
import random

def weighted_choice(items):
    total_weight = sum(w for item, w in items)
    n = random.uniform(0, total_weight)
    for item, w in items:
        if n < w:
            return item
        n = n - w
    return item
```

# Usage
The weighted_choice() function can be used to select a random item from a list of tuples containing items and their associated weights. For example:

```
items = [('apple', 10), ('banana', 5), ('orange', 20)]
selected_item = weighted_choice(items)
```

In this example, the item with the highest weight (orange) has the highest probability of being selected.
