---
title: Python implementation of a hash map
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: The Python built-in data structure dictionary can be used as a hash map.
---

**Contents**

[TOC]

Introduction to Hash Maps

Hash Map is an unordered collection of unique key-value pairs. It is also known as a dictionary, map, or associative array. The hash function is used to map the keys to their corresponding values, which makes it easy and efficient to retrieve the values from the hash map.

Creating a Hash Map

In Python, we can create a hash map using dictionaries. Here's how we can create a hash map:

```
my_dict = {
  "name": "John",
  "age": 30,
  "city": "New York"
}
```

In the above example, we have created a dictionary with three key-value pairs. The keys are "name", "age", and "city", and their corresponding values are "John", 30, and "New York", respectively.

Retrieving Values from a Hash Map

We can retrieve the values from a hash map using their corresponding keys. Here's an example:

```
my_dict = {
  "name": "John",
  "age": 30,
  "city": "New York"
}

print(my_dict["name"])
```

In the above example, we have retrieved the value of the "name" key from the hash map and printed it. The output will be "John".

Updating and Deleting Values in a Hash Map

We can update the values of a hash map using their corresponding keys. Here's an example:

```
my_dict = {
  "name": "John",
  "age": 30,
  "city": "New York"
}

my_dict["age"] = 40

print(my_dict)
```

In the above example, we have updated the value of the "age" key to 40. The output will be:

```
{
  "name": "John",
  "age": 40,
  "city": "New York"
}
```

We can also delete values from a hash map using their corresponding keys. Here's an example:

```
my_dict = {
  "name": "John",
  "age": 30,
  "city": "New York"
}

del my_dict["city"]

print(my_dict)
```

In the above example, we have deleted the value of the "city" key from the hash map. The output will be:

```
{
  "name": "John",
  "age": 30
}
```

Conclusion

Hash maps are an efficient way to store and retrieve key-value pairs. In Python, we can use dictionaries to create hash maps. We can retrieve values from a hash map using their corresponding keys, update and delete values using their corresponding keys.
