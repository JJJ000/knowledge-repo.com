---
title: What is the method for retrieving a list of values from a dictionary?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: You can use the dict.values() method to get a list of values from a dict in Python.
---

**Contents**

[TOC]

### Using For Loop 

We can use a for loop to iterate over all the key-value pairs in the dictionary and get the values.

```python
# Create a sample dictionary
sample_dict = {
    "key1": "value1",
    "key2": "value2",
    "key3": "value3"
}

# Create an empty list
value_list = []

# Iterate over all the key-value pairs in the dictionary
for key, value in sample_dict.items():
    # Append the value to the list
    value_list.append(value)

# Print the list of values
print(value_list)
```

### Using List Comprehension

We can also use a list comprehension to get a list of values from a dictionary.

```python
# Create a sample dictionary
sample_dict = {
    "key1": "value1",
    "key2": "value2",
    "key3": "value3"
}

# Create a list of values using list comprehension
value_list = [value for key, value in sample_dict.items()]

# Print the list of values
print(value_list)
```

### Using Dictionary Values Method

The `values()` method of a dictionary can also be used to get a list of values from a dictionary.

```python
# Create a sample dictionary
sample_dict = {
    "key1": "value1",
    "key2": "value2",
    "key3": "value3"
}

# Create a list of values using the values() method
value_list = list(sample_dict.values())

# Print the list of values
print(value_list)
```

### Using Dictionary Items Method

The `items()` method of a dictionary can also be used to get a list of values from a dictionary.

```python
# Create a sample dictionary
sample_dict = {
    "key1": "value1",
    "key2": "value2",
    "key3": "value3"
}

# Create a list of values using the items() method
value_list = [item[1] for item in sample_dict.items()]

# Print the list of values
print(value_list)
```
