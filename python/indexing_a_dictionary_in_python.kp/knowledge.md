---
title: What is the process of accessing a dictionary?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To index into a dictionary in Python, use the key of the value you want to access enclosed in square brackets.
---

**Contents**

[TOC]

## Introduction
Dictionaries are an important data structure in Python. They are used to store data in key-value pairs. In this tutorial, we will discuss how to index into a dictionary in Python.

## Accessing Values in a Dictionary
To access the value associated with a key in a dictionary, you can use square brackets `[]` and the key. For example, let's say we have a dictionary called `person` with the keys `name`, `age`, and `city`:

```python
person = {'name': 'John', 'age': 25, 'city': 'New York'}
```

To access the value associated with the `name` key, we can use the following code:

```python
print(person['name'])
```

Output:
```
John
```

## Handling Non-Existent Keys
If you try to access a key that does not exist in the dictionary, you will get a `KeyError`. To avoid this error, you can use the `get()` method. The `get()` method has two arguments: the key that you want to access and a default value that will be returned if the key does not exist.

Here's an example:

```python
person = {'name': 'John', 'age': 25, 'city': 'New York'}
print(person.get('gender', 'Male'))
```

Output:
```
Male
```

In the above example, we are trying to access the value of the non-existent key `gender`, but instead of getting a `KeyError`, we get the default value `Male`.

## Conclusion
Indexing into a dictionary in Python is simple and easy. You can access the value associated with a key using square brackets `[]` and the key. If the key does not exist and you want to avoid a `KeyError`, you can use the `get()` method with a default value.
