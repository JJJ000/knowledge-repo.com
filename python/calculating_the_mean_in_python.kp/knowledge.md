---
title: Calculating the mean of a list
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: The average of a list in Python can be found using the sum() and len() functions to calculate the sum of the list and the number of items in the list, respectively, and then dividing the sum by the number of items.
---

**Contents**

[TOC]

# Section 1: Define the List

Before finding the average of a list, it is important to first define the list. A list in Python is an ordered collection of values. It can contain any type of value, including integers, strings, floats, and even other lists. 

# Section 2: Create the List

The list can be created in Python by using the square brackets [ ] and separating the items with commas. For example, the following code creates a list of integers:

```
my_list = [1, 2, 3, 4, 5]
```

# Section 3: Find the Average

The average of the list can be found by using the built-in Python function sum() and dividing it by the length of the list. For example, the following code finds the average of the list created above:

```
list_sum = sum(my_list)
list_length = len(my_list)
list_average = list_sum / list_length
print(list_average)
```

# Section 4: Output

The output of the code above will be:

```
3.0
```
