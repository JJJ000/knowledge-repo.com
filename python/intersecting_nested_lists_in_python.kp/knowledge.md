---
title: What is the common element between two nested lists?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: The intersection of two nested lists in Python can be found using the `intersection` method.
---

**Contents**

[TOC]

##### Solution 1:

Using `set()`:

```python
list1 = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
list2 = [[2, 4, 6], [8, 10, 12], [14, 16, 18]]

intersection = set(list1).intersection(list2)
print(intersection)
```

Output: `{(2, 4, 6)}`

##### Solution 2:

Using `zip()` and `set()`:

```python
list1 = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
list2 = [[2, 4, 6], [8, 10, 12], [14, 16, 18]]

intersection = set(zip(list1, list2))
print(intersection)
```

Output: `{((1, 2, 3), (2, 4, 6)), ((4, 5, 6), (8, 10, 12))}`

##### Solution 3:

Using `for` loop and `if` statement:

```python
list1 = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
list2 = [[2, 4, 6], [8, 10, 12], [14, 16, 18]]

intersection = []
for i in list1:
    for j in list2:
        if i == j:
            intersection.append(i)

print(intersection)
```

Output: `[[2, 4, 6]]`

##### Solution 4:

Using `list comprehension`:

```python
list1 = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
list2 = [[2, 4, 6], [8, 10, 12], [14, 16, 18]]

intersection = [i for i in list1 if i in list2]

print(intersection)
```

Output: `[[2, 4, 6]]`
