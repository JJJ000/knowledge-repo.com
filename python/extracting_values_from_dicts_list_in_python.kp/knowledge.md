---
title: Obtaining a collection of values from a collection of dictionaries
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use a list comprehension to extract a specific value from each dictionary in the list.
---

**Contents**

[TOC]

### Section 1: Understanding the problem
Before we can work on extracting a list of values from a list of dicts, we need to understand what the problem is asking. A list of dicts can be thought of as a list of records, where each record is represented as a dictionary with key-value pairs. Suppose we have a list of dictionaries like this:

```
records = [
    {"name": "Alice", "age": 25},
    {"name": "Bob", "age": 30},
    {"name": "Charlie", "age": 35}
]
```

If we want to extract a list of all the age values from this list, we would expect to get:

```
[25, 30, 35]
```

The problem is asking us to extract all the values associated with a particular key from a list of dictionaries.


### Section 2: Using a list comprehension
One way to extract a list of values from a list of dicts is to use a list comprehension. A list comprehension is a concise way to create a new list by iterating over an existing list and applying a transformation to each element. We can use a list comprehension to extract all the values associated with a particular key from a list of dictionaries. For example, to extract all the age values from the records above, we can do:

```
ages = [record["age"] for record in records]
```

The variable `ages` will now contain the list `[25, 30, 35]`.

We can generalize this approach to extract values associated with any key from a list of dictionaries. Suppose we have a key `k` that we want to extract from a list of dictionaries `records`. We can extract all the values associated with this key using a list comprehension like this:

```
values = [record[k] for record in records]
```

The variable `values` will now contain the list of values associated with the key `k` in the `records` list.


### Section 3: Using the map function
Another way to extract a list of values from a list of dicts is to use the `map` function. The `map` function applies a function to each element of a list and returns a new list containing the results. We can use the `map` function to extract values associated with a particular key from a list of dictionaries.

For example, to extract all the age values from the `records` list using the `map` function, we can do:

```
ages = list(map(lambda record: record["age"], records))
```

The variable `ages` will now contain the same list `[25, 30, 35]` as before.

We can generalize this approach to extract values associated with any key from a list of dictionaries. Suppose we have a key `k` that we want to extract from a list of dictionaries `records`. We can extract all the values associated with this key using the `map` function like this:

```
values = list(map(lambda record: record[k], records))
```

The variable `values` will now contain the list of values associated with the key `k` in the `records` list.


### Section 4: Conclusion
In this tutorial, we discussed how to extract a list of values from a list of dicts in Python. We showed two approaches for doing this: using a list comprehension and using the `map` function. Both approaches are similar in that they iterate over each element of the list of dictionaries and extract the desired value. The choice of which approach to use is largely a matter of personal preference. In general, list comprehensions tend to be more concise, while the `map` function can be more flexible when more complex data transformations are needed.
