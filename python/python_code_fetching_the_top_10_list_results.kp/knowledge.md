---
title: Retrieve the initial 10 outcomes from a Python array
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use slicing with [010] to fetch the first 10 elements of the list in Python.
---

**Contents**

[TOC]

### Using Slice Notation

One of the easiest ways to fetch the first 10 items from a list in Python is by using slice notation. This method is built into the language and is very efficient. Here's how you can implement it:

```python
# Create a list
my_list = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15]

# Fetch the first 10 items using slice notation
first_10 = my_list[:10]

# Print the first 10 items
print(first_10)
```

Output:
```
[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```

### Using a Loop

Another way to fetch the first 10 items from a list in Python is by using a loop. This method is more flexible because it allows you to perform additional processing on the items as they are fetched. Here's an example:

```python
# Create a list
my_list = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15]

# Loop through the first 10 items and do something with them
for item in my_list[:10]:
    print(item)
```

Output:
```
1
2
3
4
5
6
7
8
9
10
```

### Using List Comprehension

List comprehension is a concise way to fetch the first 10 items from a list in Python. This method is ideal when you need to create a new list based on the first 10 items of an existing list. Here's an example:

```python
# Create a list
my_list = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15]

# Use list comprehension to fetch the first 10 items
first_10 = [item for item in my_list[:10]]

# Print the first 10 items
print(first_10)
```

Output:
```
[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```

### Using the islice() Function

If you are working with large lists, using the `islice()` function is a more efficient way to fetch the first 10 items. This function is part of the `itertools` module and is designed specifically for this task. Here's how you can use it:

```python
# Import the islice() function from the itertools module
from itertools import islice

# Create a list
my_list = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15]

# Use the islice() function to fetch the first 10 items
first_10 = list(islice(my_list, 10))

# Print the first 10 items
print(first_10)
```

Output:
```
[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```
