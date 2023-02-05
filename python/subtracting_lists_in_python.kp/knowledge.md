---
title: What is the process for subtracting one list from another?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: You can subtract one list from another in Python by using the list comprehension syntax, i.e. [x for x in list1 if x not in list2].
---

**Contents**

[TOC]

**Using the Built-In Set Type:**

1. Create two sets, one for each list:

```python
list1 = [1, 2, 3, 4]
list2 = [2, 3, 4, 5]

set1 = set(list1)
set2 = set(list2)
```

2. Calculate the difference between the two sets:

```python
difference = set1 - set2
```

3. Convert the resulting set back into a list:

```python
difference_list = list(difference)
```

4. Print the resulting list:

```python
print(difference_list) # [1]
```

**Using List Comprehension:**

1. Create two lists, one for each set:

```python
list1 = [1, 2, 3, 4]
list2 = [2, 3, 4, 5]
```

2. Create a list comprehension to subtract the two lists:

```python
difference_list = [num for num in list1 if num not in list2]
```

3. Print the resulting list:

```python
print(difference_list) # [1]
```
