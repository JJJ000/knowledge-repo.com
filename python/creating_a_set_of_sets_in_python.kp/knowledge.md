---
title: Is it possible to generate a collection of sets within a set using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Use frozenset to create sets of sets, as sets cannot contain mutable objects like other sets.
---

**Contents**

[TOC]

## Initializing a Set of Sets

To initialize a set of sets in Python, we can use the set() method to create empty sets, and then add those empty sets to another set. This will create a set of sets, where each set within the main set is empty.

```python
my_set_of_sets = set()
my_set_of_sets.add(set())
my_set_of_sets.add(set())
```

In the code above, we first create an empty set called `my_set_of_sets`. We then add two more empty sets to this main set using the `add()` method.

## Adding Sets to the Set of Sets

To add another set to our set of sets, we can simply use the `add()` method again to add a new set to the main set.

```python
new_set = set()
my_set_of_sets.add(new_set)
```

In the code above, we create a new empty set called `new_set`, and then add it to our existing set of sets using the `add()` method.

## Adding Elements to Inner Sets

To add elements to one of the sets within our set of sets, we need to first select the set we want to add to, and then use the `add()` method to add the element.

```python
my_set_of_sets = set()
inner_set = set()
inner_set.add("apple")
inner_set.add("banana")
my_set_of_sets.add(inner_set)
```

In the code above, we create an empty set called `my_set_of_sets`, and then create a new empty set called `inner_set`. We add two elements to `inner_set` using the `add()` method, and then add `inner_set` to `my_set_of_sets` using the `add()` method.

## Retrieving Elements from Inner Sets

To retrieve elements from one of the sets within our set of sets, we first need to select the inner set, and then we can access its elements using a for loop.

```python
for inner_set in my_set_of_sets:
    for element in inner_set:
        print(element)
```

In the code above, we use a nested for loop to first select each inner set within `my_set_of_sets`, and then select each element within that set. We use the `print()` statement to output each element to the console.
