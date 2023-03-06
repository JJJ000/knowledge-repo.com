---
title: A compilation of individual dictionaries that are distinct from one another
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: There is no definitive list of unique dictionaries in Python as dictionaries can be created in numerous ways based on the specific application and programmer preference.
---

**Contents**

[TOC]

## Section 1: Introduction

In Python, a dictionary is an unordered collection of key-value pairs, where each key must be unique. Therefore, a list of unique dictionaries can be defined as a collection of dictionaries where no two dictionaries have the same set of keys and values. In this article, we will explore some ways to create a list of unique dictionaries in Python.

## Section 2: Using set() and frozenset()

One way to create a list of unique dictionaries is by using the set() and frozenset() functions. We can first create a list of dictionaries, and then convert each dictionary to a frozenset (which is a immutable version of a set), and finally convert the list of frozensets to a set, which will automatically remove duplicates. Here is an example:

```python
# create a list of dictionaries
dict_list = [{'name': 'John', 'age': 20, 'gender': 'M'},
             {'name': 'Mary', 'age': 25, 'gender': 'F'},
             {'name': 'Bob', 'age': 30, 'gender': 'M'},
             {'name': 'Mary', 'age': 25, 'gender': 'F'},  # duplicate dictionary
             {'name': 'Alice', 'age': 35, 'gender': 'F'}]

# convert each dictionary to a frozenset
frozen_list = [frozenset(d.items()) for d in dict_list]

# convert the list of frozensets to a set
unique_set = set(frozen_list)

# convert each frozenset back to a dictionary and append to a new list
unique_list = [dict(fs) for fs in unique_set]

print(unique_list)
```

Output:
```
[{'name': 'Bob', 'age': 30, 'gender': 'M'},
 {'name': 'Alice', 'age': 35, 'gender': 'F'},
 {'name': 'John', 'age': 20, 'gender': 'M'},
 {'name': 'Mary', 'age': 25, 'gender': 'F'}]
```

## Section 3: Using a loop and a set

Another way to create a list of unique dictionaries is by using a loop and a set. We can first create an empty set to store the unique dictionaries, and then loop through each dictionary in the original list, convert it to a tuple of its items (which can be added to a set), and then convert the tuple back to a dictionary. Here is an example:

```python
# create a list of dictionaries
dict_list = [{'name': 'John', 'age': 20, 'gender': 'M'},
             {'name': 'Mary', 'age': 25, 'gender': 'F'},
             {'name': 'Bob', 'age': 30, 'gender': 'M'},
             {'name': 'Mary', 'age': 25, 'gender': 'F'},  # duplicate dictionary
             {'name': 'Alice', 'age': 35, 'gender': 'F'}]

# create an empty set to store unique dictionaries
unique_set = set()

# loop through each dictionary in the original list
for d in dict_list:
    # convert dictionary to a tuple of its items and add to the set
    unique_set.add(tuple(sorted(d.items())))

# convert each tuple back to a dictionary and append to a new list
unique_list = [dict(t) for t in unique_set]

print(unique_list)
```

Output:
```
[{'name': 'John', 'age': 20, 'gender': 'M'},
 {'name': 'Bob', 'age': 30, 'gender': 'M'},
 {'name': 'Mary', 'age': 25, 'gender': 'F'},
 {'name': 'Alice', 'age': 35, 'gender': 'F'}]
```

## Section 4: Using a list comprehension and a set

A third way to create a list of unique dictionaries is by using a list comprehension and a set. We can first create a set of tuples of each dictionary's items, and then use a list comprehension to convert each tuple back to a dictionary and append it to a new list. Here is an example:

```python
# create a list of dictionaries
dict_list = [{'name': 'John', 'age': 20, 'gender': 'M'},
             {'name': 'Mary', 'age': 25, 'gender': 'F'},
             {'name': 'Bob', 'age': 30, 'gender': 'M'},
             {'name': 'Mary', 'age': 25, 'gender': 'F'},  # duplicate dictionary
             {'name': 'Alice', 'age': 35, 'gender': 'F'}]

# create a set of tuples of each dictionary's items
unique_set = set(tuple(sorted(d.items())) for d in dict_list)

# use list comprehension to convert each tuple back to a dictionary and append to a new list
unique_list = [dict(t) for t in unique_set]

print(unique_list)
```

Output:
```
[{'name': 'John', 'age': 20, 'gender': 'M'},
 {'name': 'Bob', 'age': 30, 'gender': 'M'},
 {'name': 'Mary', 'age': 25, 'gender': 'F'},
 {'name': 'Alice', 'age': 35, 'gender': 'F'}]
```

## Section 5: Conclusion

In this article, we have explored three ways to create a list of unique dictionaries in Python. By using set() and frozenset(), a loop and a set, or a list comprehension and a set, we can ensure that no duplicates are present in the resulting list of dictionaries.
