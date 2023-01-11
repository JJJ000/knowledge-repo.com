---
title: What is the procedure for deleting a key from a Python dictionary?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-11 00:00:00
updated_at: 2023-01-11 00:00:00
tldr: You can remove a key from a Python dictionary by using the `del` keyword.
---

**Contents**

[TOC]

### Using the `del` Statement
The `del` statement can be used to remove a key from a Python dictionary. It takes the form `del dict[key]`, where `dict` is the name of the dictionary and `key` is the key to be removed.

For example, if we have a dictionary `my_dict`:

```python
my_dict = {'name': 'John', 'age': 25, 'city': 'New York'}
```

We can remove the key `'age'` from the dictionary with the following statement:

```python
del my_dict['age']
```

The dictionary would then look like this:

```python
my_dict = {'name': 'John', 'city': 'New York'}
```

### Using the `pop()` Method
The `pop()` method can also be used to remove a key from a Python dictionary. It takes the form `dict.pop(key)`, where `dict` is the name of the dictionary and `key` is the key to be removed.

For example, if we have a dictionary `my_dict`:

```python
my_dict = {'name': 'John', 'age': 25, 'city': 'New York'}
```

We can remove the key `'age'` from the dictionary with the following statement:

```python
my_dict.pop('age')
```

The dictionary would then look like this:

```python
my_dict = {'name': 'John', 'city': 'New York'}
```

### Using the `popitem()` Method
The `popitem()` method can also be used to remove a key from a Python dictionary. It takes the form `dict.popitem()`, where `dict` is the name of the dictionary.

For example, if we have a dictionary `my_dict`:

```python
my_dict = {'name': 'John', 'age': 25, 'city': 'New York'}
```

We can remove a random key from the dictionary with the following statement:

```python
my_dict.popitem()
```

The dictionary would then look like this, with one of the keys removed:

```python
my_dict = {'name': 'John', 'city': 'New York'}
```

### Using the `clear()` Method
The `clear()` method can also be used to remove all keys from a Python dictionary. It takes the form `dict.clear()`, where `dict` is the name of the dictionary.

For example, if we have a dictionary `my_dict`:

```python
my_dict = {'name': 'John', 'age': 25, 'city': 'New York'}
```

We can remove all keys from the dictionary with the following statement:

```python
my_dict.clear()
```

The dictionary would then be empty:

```python
my_dict = {}
```
