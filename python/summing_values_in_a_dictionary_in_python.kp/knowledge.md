---
title: What is the procedure for calculating the total of all entries in a dictionary?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: To sum all the values in a dictionary in Python, use the built-in sum() function on the dictionary`s values.
---

**Contents**

[TOC]

# Section 1: Prerequisites

Before attempting to sum all the values in a dictionary, it is important to understand the following concepts:

1. What is a dictionary?
2. What is the syntax for accessing values in a dictionary?

# Section 2: Creating a Dictionary

To begin, we must create a dictionary that contains the values we would like to sum. This can be done using the following syntax:

```
my_dict = {
    'key1': value1,
    'key2': value2,
    'key3': value3
}
```

# Section 3: Summing the Values

Once we have our dictionary, we can use the built-in `sum()` function to calculate the sum of all the values in the dictionary. To do this, we must pass the dictionary to the `sum()` function, along with the `values()` method to get the list of values from the dictionary:

```
total = sum(my_dict.values())
```

# Section 4: Outputting the Result

Finally, we can print the result of the sum to the console using the `print()` function:

```
print(total)
```
