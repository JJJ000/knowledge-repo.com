---
title: Choose 50 items randomly from the given list
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Use the `random.sample()` function from the `random` module to select 50 items from a list at random in Python.
---

**Contents**

[TOC]

## Step 1: Import Libraries

First, we need to import the `random` library which will be used to select random items from the list.

```python
import random
```

## Step 2: Define List

Next, we need to define the list which we will select items from. For the purpose of this example, we will use a list of numbers from 1 to 100.

```python
my_list = [x for x in range(1, 101)]
```

## Step 3: Randomly Select Items

Finally, we will use the `random.sample()` function to select 50 random items from the list. This function takes two arguments: the list to select from, and the number of items to select.

```python
selected_items = random.sample(my_list, 50)
```

Now `selected_items` contains a list of 50 random items selected from the original list.

## Putting it All Together

Here is the complete code to select 50 items from a list at random:

```python
import random

my_list = [x for x in range(1, 101)]
selected_items = random.sample(my_list, 50)
```
