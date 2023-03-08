---
title: What is the process of adding elements from an iterable to a set?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: You can use the update() method to add the contents of an iterable to a set in Python.
---

**Contents**

[TOC]

## Converting iterable to a set

Before adding the contents of an iterable to a set, we first need to convert the iterable into a set so that we can combine the unique elements.

To convert an iterable into a set, we simply pass it into the `set()` constructor like so:

```python
my_iterable = [1, 2, 3, 3, 4, 5]
my_set = set(my_iterable)
```

Here, we have converted the iterable `my_iterable` into a set of `{1, 2, 3, 4, 5}`.

## Adding set elements to a set

To add one set to another, we can use the `update()` method which takes an iterable as its argument:

```python
set_one = {1, 2, 3}
set_two = {4, 5, 6}

set_one.update(set_two)
```

Here, we have added `set_two` to `set_one` using the `update()` method. The resulting set is `{1, 2, 3, 4, 5, 6}`.

## Combining iterables into a set

If we have several iterables that we want to combine into one set, we can first convert each iterable to a set, and then use the `update()` method to add them all to a new set:

```python
iterable_one = [1, 2, 3]
iterable_two = [3, 4, 5]
iterable_three = [5, 6, 7]

set_one = set(iterable_one)
set_one.update(iterable_two)
set_one.update(iterable_three)
```

Here, we have converted each iterable to a set and used the `update()` method to add them all to `set_one`. The resulting set is `{1, 2, 3, 4, 5, 6, 7}`.

## Adding iterables to existing set

If we already have a set, and we want to add the contents of an iterable to it, we can use the `update()` method once again:

```python
my_set = {1, 2, 3}
my_iterable = [3, 4, 5]

my_set.update(my_iterable)
```

Here, we have added the contents of `my_iterable` to `my_set` using the `update()` method. The resulting set is `{1, 2, 3, 4, 5}`.
