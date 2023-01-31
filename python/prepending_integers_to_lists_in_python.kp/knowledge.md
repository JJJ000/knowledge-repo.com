---
title: Prepend an integer to the start of a list in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: list.insert(0, integer)
---

**Contents**

[TOC]

**Option 1**

Using `list.insert()`

1. Create a list:

```python
my_list = [1, 2, 3]
```

2. Use `list.insert()` to insert an element at the beginning of the list:

```python
my_list.insert(0, 4)
```

3. Print the list to verify the result:

```python
print(my_list)
```

Output:

```
[4, 1, 2, 3]
```

**Option 2**

Using `list.append()` and `list.reverse()`

1. Create a list:

```python
my_list = [1, 2, 3]
```

2. Use `list.append()` to add an element to the end of the list:

```python
my_list.append(4)
```

3. Use `list.reverse()` to reverse the list:

```python
my_list.reverse()
```

4. Print the list to verify the result:

```python
print(my_list)
```

Output:

```
[4, 3, 2, 1]
```
