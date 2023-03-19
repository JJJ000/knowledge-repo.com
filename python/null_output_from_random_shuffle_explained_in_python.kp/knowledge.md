---
title: What is the reason for random.shuffle not returning any value?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: random.shuffle shuffles the list in place, so it does not need to return a new list and returns None to indicate that the list has been shuffled.
---

**Contents**

[TOC]

# Introduction

`random.shuffle` is a function in Python's `random` module that shuffles the elements of a list randomly. However, it is peculiar that this function returns `None` instead of the shuffled list. 

In this article, we will explore the reasons why `random.shuffle` returns `None` in Python. 

# In-place shuffling

The primary reason why `random.shuffle` returns `None` is that it shuffles the elements of the list in-place, i.e., it modifies the original list instead of creating a new one. The `None` return value serves as a reminder that the function does not return a new list or any value. 

If you assign the shuffled list to a variable, the output will be `None`. However, the original list will be shuffled as expected. 

```python
>>> import random
>>> my_list = [1, 2, 3, 4, 5]
>>> shuffled_list = random.shuffle(my_list)
>>> shuffled_list     
>>> # Output: None
>>> my_list         
>>> # Output: [4, 1, 3, 5, 2]
```

# Save memory

Returning `None` rather than creating and returning a copy of the shuffled list saves memory. Since the original list is shuffled in-place, it is unnecessary to create a copy of the list. Thus, returning `None` helps to reduce memory usage, especially if shuffling large lists. 

# Consistency with other Python built-in functions

Returning `None` is consistent with other Python built-in functions like `sort` and `reverse`, which also modify the list in-place rather than returning a new one. The primary difference between `shuffle` and these other list methods is that the latter two sort or reverse the list in ascending or descending order, respectively. 

# Conclusion 

In summary, `random.shuffle` returns `None` because it shuffles the list in-place, saving memory and being consistent with other Python built-in functions like `sort` and `reverse`. Although it might be confusing at first, it is essential to understand that the function modifies the original list rather than creating a new one.
