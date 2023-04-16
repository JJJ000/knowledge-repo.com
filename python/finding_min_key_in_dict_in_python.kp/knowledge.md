---
title: Find the key with the smallest value in a dictionary
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The key corresponding to the minimum value within a dictionary can be found by using the min() function.
---

**Contents**

[TOC]

# Section 1: Finding the Minimum Value

To find the minimum value within a dictionary in Python, we can use the `min()` function. This function takes a dictionary as an argument and returns the minimum value within the dictionary. 

# Section 2: Finding the Corresponding Key

Once we have the minimum value, we can use the `dict.items()` method to get the key corresponding to the minimum value. This method returns a list of tuples, where each tuple contains a key-value pair from the dictionary. We can then loop through the list of tuples and check if the value in each tuple matches the minimum value. If it does, then we can return the corresponding key. 

# Section 3: Example

Let's look at an example. Suppose we have a dictionary: 

```
my_dict = {
    'a': 5,
    'b': 2,
    'c': 10
}
```

We can find the minimum value using the `min()` function: 

```
min_val = min(my_dict.values())
```

Now, we can use the `dict.items()` method to find the corresponding key:

```
for key, value in my_dict.items():
    if value == min_val:
        min_key = key
```

In this example, `min_key` will be equal to `'b'`. 

# Section 4: Summary

In summary, to find the key corresponding to the minimum value within a dictionary in Python, we can use the `min()` function to find the minimum value, and then use the `dict.items()` method to loop through the dictionary and find the corresponding key.
