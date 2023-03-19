---
title: Retrieve the initial element from every sub-list
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: To extract the first item of each sublist in Python, use a list comprehension with indexing.
---

**Contents**

[TOC]

## Using list comprehension

List comprehension is a concise and efficient way to create a list. We can use list comprehension to extract the first item of each sublist. 


```python
list_of_lists = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]

first_items = [sublist[0] for sublist in list_of_lists]

print(first_items)
```

Output: 

```
[1, 4, 7]
```


## Using map function

The map function can also be used to extract the first item of each sublist. This approach allows for more complex operations on the list elements.


```python
list_of_lists = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]

first_items = list(map(lambda x: x[0], list_of_lists))

print(first_items)
```

Output: 

```
[1, 4, 7]
```


## Using a for loop

A for loop can also be used to extract the first item of each sublist. This approach offers the advantage of being easy to understand for new programmers.


```python
list_of_lists = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]

first_items = []

for sublist in list_of_lists:
    first_items.append(sublist[0])

print(first_items)
```

Output: 

```
[1, 4, 7]
```
