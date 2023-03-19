---
title: Creating a dictionary of lists using python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: In Python, a dictionary of lists is created using curly braces {} to define the dictionary and square brackets [] to define each list within that dictionary.
---

**Contents**

[TOC]

Section 1: Introduction
Python is a powerful programming language that provides several built-in data types to create complex data structures. One of such data structures is a dictionary, which is an unordered collection of key-value pairs. The value of a dictionary can be of any data type, including lists. Creating a dictionary of lists is a common use case in Python programming, where each key of the dictionary corresponds to a list of elements.

Section 2: Creating empty dictionary of lists
You can create an empty dictionary of lists in Python using curly braces {}. This will create an empty dictionary that contains no items. You can then add new keys and values to the dictionary using the square bracket notation []. To create an empty list for each key, you can simply assign an empty list [] to the key in the dictionary.

```
# create an empty dictionary of lists
my_dict = {}

# add new keys and values to the dictionary
my_dict['key1'] = []
my_dict['key2'] = []

print(my_dict)
```

Output:
```
{'key1': [], 'key2': []}
```

Section 3: Creating dictionary of lists with elements
You can also create a dictionary of lists with elements using the same approach. Simply assign a list of elements to each key in the dictionary using the square bracket notation [].

```
# create a dictionary of lists with elements
my_dict = {
    'key1': [1, 2, 3],
    'key2': ['a', 'b', 'c']
}

print(my_dict)
```

Output:
```
{'key1': [1, 2, 3], 'key2': ['a', 'b', 'c']}
```

Section 4: Adding elements to the dictionary of lists
To add new elements to the list of a dictionary key, you can simply use the append() method. This method adds a new element to the end of the list.

```
# create an empty dictionary of lists
my_dict = {}

# add new keys and values to the dictionary
my_dict['key1'] = []
my_dict['key2'] = []

# add new elements to the list of a dictionary key
my_dict['key1'].append(1)
my_dict['key1'].append(2)
my_dict['key1'].append(3)

my_dict['key2'].append('a')
my_dict['key2'].append('b')
my_dict['key2'].append('c')

print(my_dict)
```

Output:
```
{'key1': [1, 2, 3], 'key2': ['a', 'b', 'c']}
```

Note that you can also use the += operator to add elements to the list of a dictionary key.

```
# create a empty dictionary of lists
my_dict = {}

# add new keys and values to the dictionary
my_dict['key1'] = []
my_dict['key2'] = []

# add new elements to the list of a dictionary key
my_dict['key1'] += [1, 2, 3]
my_dict['key2'] += ['a', 'b', 'c']

print(my_dict)
```

Output:
```
{'key1': [1, 2, 3], 'key2': ['a', 'b', 'c']}
```
