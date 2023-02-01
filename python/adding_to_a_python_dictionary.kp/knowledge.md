---
title: Insert a new key-value pair into a dictionary in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Dictionaries in Python are mutable, so you can add a new item by using the syntax dictionary\_name[key] = value.
---

**Contents**

[TOC]

### Adding an Item

To add an item to a dictionary in Python, you can use the `update()` method. This method takes a `key` and a `value` as parameters and adds the key-value pair to the dictionary.

```python
# Create a dictionary
my_dict = {
    "name": "John",
    "age": 25
}

# Add a new item
my_dict.update({"gender": "male"})

# Output the updated dictionary
print(my_dict)
```

Output:

```
{'name': 'John', 'age': 25, 'gender': 'male'}
```

### Updating an Existing Item

You can also use the `update()` method to update an existing item in a dictionary. This is done by providing the same `key` with a new `value`.

```python
# Create a dictionary
my_dict = {
    "name": "John",
    "age": 25
}

# Update an existing item
my_dict.update({"age": 26})

# Output the updated dictionary
print(my_dict)
```

Output:

```
{'name': 'John', 'age': 26}
```

### Adding Multiple Items

The `update()` method can also be used to add multiple items to a dictionary in one go. This is done by passing a dictionary as the argument to the `update()` method.

```python
# Create a dictionary
my_dict = {
    "name": "John",
    "age": 25
}

# Add multiple items
my_dict.update({
    "gender": "male",
    "city": "New York"
})

# Output the updated dictionary
print(my_dict)
```

Output:

```
{'name': 'John', 'age': 25, 'gender': 'male', 'city': 'New York'}
```
