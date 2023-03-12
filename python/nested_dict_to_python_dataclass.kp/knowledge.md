---
title: Creating a Python dataclass using a nested dictionary
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Using the `dataclass` decorator with the `field` function and a recursive function that converts nested dicts to objects, we can automatically create a Python dataclass from a nested dict.
---

**Contents**

[TOC]

# Introduction

In Python, dataclasses provide a way to define classes quickly and concisely with just a few lines of code. This is especially useful when dealing with complex data structures that require multiple levels of nesting. In this article, we will explore how to create a Python dataclass from a nested dictionary.

# Converting a nested dictionary to a dataclass

To create a dataclass from a nested dictionary, we need to perform the following steps:

1. Parse the nested dictionary and extract the fields
2. Create a new dataclass with the extracted fields
3. Populate the dataclass fields with the values from the nested dictionary

Here’s a code snippet that demonstrates how to perform these steps:

```python
from dataclasses import dataclass, field
from typing import List

@dataclass
class Person:
    name: str
    age: int

@dataclass
class Company:
    name: str
    employees: List[Person] = field(default_factory=list)


def create_dataclass(data: dict):
    # Parse the dictionary and extract the fields
    name = data['name']
    employees = []
    for person_data in data['employees']:
        person = Person(**person_data)
        employees.append(person)

    # Create a new dataclass with the extracted fields
    company = Company(name=name, employees=employees)

    return company
```

In this implementation, we first define two dataclasses: `Person` and `Company`. We then define the `create_dataclass` function that takes a dictionary as input and returns a `Company` instance.

The `create_dataclass` function first extracts the necessary fields from the input dictionary and constructs a list of `Person` instances from the nested `employees` dictionary.

It then creates a new instance of the `Company` dataclass with the extracted fields and returns it.

# Conclusion

In conclusion, we have seen how to create a Python dataclass from a nested dictionary. This approach is useful when dealing with complex data structures that require multiple levels of nesting. We can easily parse the nested dictionary, extract the necessary fields, and create a new dataclass instance from them.
