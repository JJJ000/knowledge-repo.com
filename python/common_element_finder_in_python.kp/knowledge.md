---
title: Determine the element that appears most frequently within a given list
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: To find the most common element in a list in Python, you can use the `max()` function with `key` set to `list.count`.
---

**Contents**

[TOC]

## Approach 1: Using the max() function and key parameter

One of the simplest ways to find the most common element in a list is to use the built-in `max()` function with the `key` parameter. We can use this approach to find the element that appears the most times in a list.

```python
lst = [1, 2, 3, 4, 2, 3, 3, 4, 4, 4]
most_common_element = max(set(lst), key=lst.count)
print(most_common_element)
```

Output:
```
4
```

Here, we first convert the list to a set to remove any duplicate elements. Then, we use the `max()` function with the `key` parameter set to `lst.count` – the number of times an element appears in the original list. This will return the element that appears the most number of times in the list.


## Approach 2: Using the Counter() function from the collections module

Another easy way to find the most common element in a list is to use the `Counter()` function from the `collections` module. This function takes an iterable (like a list) and returns a dictionary with the count of each distinct element in it.

```python
from collections import Counter

lst = [1, 2, 3, 4, 2, 3, 3, 4, 4, 4]
counter = Counter(lst)
most_common_element = counter.most_common(1)[0][0]
print(most_common_element)
```

Output:
```
4
```

Here, we create a `Counter()` object from the list `lst`. We can then use the `most_common()` method of this object to get a list of the most common elements and their counts. In this case, we only want the single most common element, so we pass the argument `1` to this method. Finally, we extract the element itself from the tuple returned by `most_common()`.


## Approach 3: Using a dictionary and a loop

We can also find the most common element in a list by looping over the list and keeping track of the count of each element in a dictionary. We can then find the element with the highest count in the dictionary.

```python
lst = [1, 2, 3, 4, 2, 3, 3, 4, 4, 4]
count_dict = {}

for element in lst:
    if element in count_dict:
        count_dict[element] += 1
    else:
        count_dict[element] = 1

most_common_element = max(count_dict, key=count_dict.get)
print(most_common_element)
```

Output:
```
4
```

Here, we first create an empty dictionary `count_dict` to store the count of each element. We then loop over the list `lst` and update the count of each element in the dictionary. Finally, we use the `max()` function with the `key` parameter set to `count_dict.get` – the value (i.e. count) associated with each element in the dictionary. This will return the element with the highest count, which is the most common element.
